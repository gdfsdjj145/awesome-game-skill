---
name: escalating-shop-sink
description: Design an Escalating Shop Sink for card removal / deck thinning in roguelike deckbuilders (15 -> 20 -> 25 -> 30 escalating price ladder, once-per-shop cap, hard MIN_DECK=5 floor, and intentional price crossover above Rare Relics on purge #3). Use when building shops, economy sinks, or curing deck bloat without enabling 5-card infinite loops.
---

# Escalating Shop Sink Contract (Deck Removal Economy)

Never treat deck removal as an afterthought. Two naive extremes immediately break a roguelike deckbuilder:
1. **No removal**: Mid-to-late runs bloat to 28–35 cards; your signature UR card drops to ~13% draw rate and builds feel sluggish.
2. **Free or cheap removal**: Players strip down to 5 cards and lock into a deterministic Turn-1 infinite loop that trivializes every boss.

The proven solution is an **Escalating Subtraction Sink** — removal that feels affordable at first, then deliberately hurts more than buying a rare relic.

## 1. The 5 Core Economy Rules

1. **Escalating Run-Wide Cost Ladder**:
   - `cost = BASE_COST + STEP_COST * run.shopPurgesUsed`
   - Proven baseline (from Zhaoshi Wulin A3): `BASE_COST = 15`, `STEP_COST = 5` (`15 -> 20 -> 25 -> 30...`).
   - Persist `run.shopPurgesUsed` across the entire run and across save/reload — **never reset per shop**.
2. **Once-Per-Shop Hard Cap**:
   - Each shop node allows at most `1` card removal (`shop.purgeUsed = true`) so rich players cannot dump gold to strip 4 cards in one room.
3. **Hard Floor Guard (`MIN_DECK = 5`)**:
   - Allow removing starter basic cards, but disable removal whenever `deck.length <= MIN_DECK` (default `5`, matching or slightly exceeding standard 4-card draw size) to prevent empty draws and trivial 1-turn infinites.
4. **Intentional Price Crossover Against Rare Relics**:
   - Calibrate `BASE_COST + 2 * STEP_COST` (the **3rd purge**, e.g. `25` coins) to exceed a **Shop Rare Relic** (e.g. `20` coins).
   - Purges #1–#2 (`15 / 20`) cleanly clear starter junk; Purge #3 (`25`) forces a genuine sweaty trade-off between **consistency (purge)** and **power spike (relic)**.
5. **Keep Campfire & Events Distinct**:
   - Keep Campfire focused on Heal vs Upgrade (do not dilute Campfire with cheap free purges). Reserve 1–2 rare seeded Events for occasional bonus removals.

## 2. Verification Checklist
- [ ] Removing cards increases `run.shopPurgesUsed` and persists identically after saving and reloading.
- [ ] Every shop strictly locks removal after 1 use in that room.
- [ ] When `deck.length === MIN_DECK`, removal is disabled with a clear UI reason.
- [ ] On purge #3, removal price strictly exceeds the shop's Rare Relic benchmark price.
- [ ] Simulated 3-extreme check confirms key-card draw rate rises from ~13% (bloat) into the 30%–55% healthy zone without allowing sub-5-card loops.
