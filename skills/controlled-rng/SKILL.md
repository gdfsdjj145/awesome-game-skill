---
name: controlled-rng-dealer
description: Implement a 3-slot Controlled RNG reward dealer for roguelike deckbuilders and loot games (Synergy slot + Wild slot + Pity/Rarity slot) with display shuffle, elite floor guarantees, and 1000-roll distribution checks. Use when designing card rewards, shop offers, or roguelike draft pools that feel lucky without hard-locking builds.
---

# Controlled RNG 3-Slot Reward Dealer

Never ship raw uniform random card rewards in a roguelike deckbuilder. Raw RNG produces miserable dry streaks where a player building an archetype sees zero synergy cards for 3+ fights and rage-quits.

Instead, separate **build support**, **discovery**, and **rarity excitement** into 3 dedicated slots, then shuffle their display order so the player feels lucky instead of reading the math.

## 1. The 3-Slot Contract (No Duplicates)

When rolling a 3-card reward pack from the run's unlocked pool:

1. **Slot 1 — Synergy Slot (Non-Rare Pool)**
   - Exclude `rare` cards so Slot 1 cannot steal excitement from the Rarity/Pity slot.
   - Count matching archetype tags already in the player's deck: `bonus = sum(deckTagCounts[tag] for tag in card.tags)`.
   - Assign weight: `weight = min(SYNERGY_CAP, 1 + SYNERGY_STEP * bonus)`.
   - Default proven values: `SYNERGY_STEP = 2`, `SYNERGY_CAP = 7`.
   - **Why cap at 7?** Without a cap, players get force-fed the exact same archetype every fight and runs feel scripted. Capping at 7 gives strong momentum while preserving room to pivot.

2. **Slot 2 — Wild Slot (Non-Rare Pool)**
   - Exclude `rare` cards and Slot 1's picked card.
   - Sample **uniformly at random** across remaining non-rare cards.
   - **Why keep one pure random slot?** It creates surprise pivots, hybrid combos, and prevents every run from collapsing into one linear recipe.

3. **Slot 3 — Rarity & Pity Slot (Full Pool)**
   - Exclude cards already picked in Slots 1 & 2.
   - Compute current rare probability:
     `rareChance = min(RARE_CAP, RARE_BASE + RARE_PITY_STEP * run.rareMisses)`
   - Default proven values:
     - `RARE_BASE = 0.10` (10%)
     - `RARE_PITY_STEP = 0.03` to `0.05` (+3% for long 40-node runs, +5% for shorter runs)
     - `RARE_CAP = 0.60` (60%)
     - `UNCOMMON_CHANCE = 0.30` (30%)
   - Roll `u = randf()`:
     - `u < rareChance` -> `rare`
     - `elite || u < rareChance + UNCOMMON_CHANCE` -> `uncommon` (Elites guarantee at least Uncommon!)
     - otherwise -> `common`
   - Fallback gracefully through `[want, uncommon, common, rare]` if a tier is exhausted.
   - After rolling: if any offered card is `rare`, reset `run.rareMisses = 0`; otherwise increment `run.rareMisses += 1`.

4. **Fisher-Yates Display Shuffle (Mandatory)**
   - Shuffle the final 3 cards before showing them to the player.
   - Never leave Synergy always on the left and Rare always on the right — players will spot the pattern in 10 minutes and the illusion breaks.

## 2. Verification Checklist (Run Before Merging)
- [ ] **Zero duplicates**: Across 1,000 simulated packs, every pack has 3 unique card IDs.
- [ ] **Synergy lift**: With 3 cards of Tag A in deck, Tag A appears in at least 1 of the 3 slots >55% of deals (vs ~25–35% under pure random), yet non-Tag-A cards still appear in >95% of deals.
- [ ] **Pity reset**: `rareMisses` strictly increments on non-rare packs and resets to 0 immediately when a rare is offered.
- [ ] **Elite floor**: Across 500 elite rolls, Slot 3 never outputs a `common` card when `uncommon`/`rare` cards exist.
- [ ] **Position entropy**: Across 1,000 packs, rare cards appear roughly ~33% in index 0, ~33% in index 1, ~33% in index 2.
