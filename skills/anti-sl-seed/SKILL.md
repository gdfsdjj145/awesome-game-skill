---
name: deterministic-seed-anti-sl
description: Implement Deterministic Seed Anti-Save-Scumming for roguelikes and single-player strategy games — lock gambling, card rewards, and shop rerolls to hash(runSeed, nodeId) at room entry while intentionally preserving a combat retry seam ("prevent farming, forgive misclicks"). Use when designing save persistence, seeded RNG streams, or event outcomes.
---

# Deterministic Seed & The Anti-SL Seam

Do not let single-player roguelike players Alt+F4 to reroll gambling events, chest drops, or shop refreshes — free infinite save-scumming turns thrilling risk-reward into a joyless chore. Equally, do **not** ironman-lock every combat misclick.

## 1. Core Architecture (Pure RNG Lock + Skill Retry Seam)

1. **Derive Node-Scoped Seeded Streams**:
   - Store one immutable `run.seed` at run start.
   - For every map node, compute `node.roll = hash(run.seed, act, floor, nodeIndex)` when the map is generated or the node is entered.
   - Use isolated salted streams per system (`node.roll + 31` for events, `node.roll + 73` for shop inventory, `node.roll + 109` for loot) so actions in one UI cannot shift RNG elsewhere.
2. **Precompute & Persist Pure-RNG Outcomes On Entry**:
   - Compute event gambles (e.g., 50% win +15G / lose -10G), card reward packs, and shop reroll offers **before** the player clicks, and persist the node's resolution state immediately on choice.
   - Reloading 1×, 10×, or 100× inside the same node MUST produce the exact same dice roll, card trio, and shop roll.
3. **Preserve the Combat Retry Seam ("Anti-Grind, Pro-Skill")**:
   - Checkpoint save at **battle start** with the battle's draw-order seed fixed.
   - If a player fat-fingers a card or misreads a boss telegraph and restarts the game, let them replay that battle from Turn 1 with the **same draw order** — they can fix tactical misplays, never farm luck.
4. **Never Mix Global `Math.random()` / `randf()`**:
   - Ban unseeded global RNG calls inside events, shops, and draft dealers.

## 2. Verification Checklist
- [ ] Entering a gambling event and force-reloading 10 times produces identical win/lose outcomes and dice rolls every time.
- [ ] Moving to the next room (`nodeId + 1`) produces an independent outcome without affecting prior nodes.
- [ ] Shop rerolls persist their new state immediately after spending gold so reload cannot refund and re-roll.
- [ ] Reloading mid-combat restarts the encounter cleanly at Turn 1 using the exact same deterministic draw order.
