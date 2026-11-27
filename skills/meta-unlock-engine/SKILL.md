---
name: progressive-meta-unlock-engine
description: Build a 3-layer Progressive Meta-Unlock Engine for roguelikes (40+30 Starter/Exploration Relic Split with Zero Base-Stat Inflation, Dual-Track XP Pity + Mastery Shortcut Unlocking, and ×3.5 Fresh Spotlight Weighting for the next 2 runs). Use when designing roguelike meta-progression that hooks players with new builds instead of stat grinds.
---

# 3-Layer Progressive Meta-Unlock Engine

Never dump all 70+ relics and complex build cards on Run 1 — newcomers drown in diluted pools and quit after 3 runs. And never lock raw `+10% ATK / +20% HP` behind meta-grinds that ruin first-run balance.

## 1. The 3-Layer Contract

1. **Layer 1 — 40 + 30 Pool Split & Zero Stat Inflation**:
   - Ship **~55–60% intuitive, zero-pop-up starter relics** (e.g. `40/70`) unlocked from Run 1 so early runs feel clean and readable.
   - Gate the remaining **~40% complex / synergy-heavy relics** (`30/70`) and themed Hero Scrolls (e.g. `4` tiers × `4–5` cards per hero) behind progressive exploration.
   - **Hard rule**: Meta unlocks expand *horizontal build depth* (archetypes, combo tools, cross-role curios) — **zero** permanent base Attack or HP multipliers.
2. **Layer 2 — Dual-Track Unlocking (Never Hard-Stuck)**:
   - Every progression tier supports **BOTH** paths (whichever fires first):
     - **Pity Track (Journey XP)**: Granted at run end even on defeats, unlocking along escalating milestones (proven curve: `100 -> 240 -> 420 -> 640 XP`). Casual players always make progress.
     - **Mastery Shortcut Track**: Instant early unlock when skilled players pull off a signature play (e.g., `Block 20 DMG`, `Play 3 Attacks in 1 Turn`, `Defeat Region 2 Boss`).
   - Commit unlocks strictly at terminal run resolution (or verified milestone checkpoints) and maintain 100% legacy save compatibility.
3. **Layer 3 — Fresh Spotlight Weighting (`×3.0–3.5` for Next 2 Runs)**:
   - Track newly unlocked card/relic IDs in `meta.fresh[itemId] = 2` (remaining runs).
   - During the next **2 runs**, multiply their draft/drop weight by `CARD_FRESH_WEIGHT_MULT = 3.0` and `RELIC_FRESH_WEIGHT_MULT = 3.5`, and tag them with a subtle `✦ Fresh Unlock` badge.
   - Decrement remaining runs automatically so items blend seamlessly back to `×1.0` once the player has experienced them.

## 2. Verification Checklist
- [ ] Fresh save exposes exactly the starter pool (e.g. 40 relics) with zero permanent ATK/HP stat upgrades.
- [ ] Losing a run still awards Journey XP and unlocks Tier 1 once XP reaches `100`.
- [ ] Completing a Mastery Shortcut unlocks its Scroll immediately even when Journey XP is below threshold.
- [ ] Across 50 simulated post-unlock runs, newly unlocked items appear at `>= 2.5×` baseline rate during Spotlight runs and return strictly to `1.0×` after 2 runs.
