---
name: puzzle-curve-solver
description: Design and verify viral peel-and-match / pixel-flow / knit-unravel casual puzzle levels with exact color conservation, perimeter BFS exposure, a bounded heuristic DFS 5-slot solvability proof, and Monte Carlo blind-bot difficulty curve tuning (100% -> 82% -> 58% -> 36%). Use whenever building slot-based casual puzzles that must feel tense without unwinnable deadlocks.
---

# Solvable Puzzle Curve & Blind-Bot Difficulty Tuner

Casual peel-and-match puzzles (*Pixel Flow*, *Knit Out*, *Yarn Unravel*, *Sheep-a-Sheep*) fail for two opposite reasons: naive random shuffles produce **0% unwinnable deadlocks**, while un-tuned outer-to-inner generation feels like mindless 100% tapping.

## 1. The 4-Gate Level Engineering Contract

1. **Exact Color Conservation**:
   - Assert `sum(boardBites[color]) === sum(trayBoxCapacity[color])` for every color (including double-layer ice knots and multi-cell big blocks). Fail CI immediately on any mismatch.
2. **Perimeter BFS Exposure (`computeExposure`)**:
   - Flood-fill reachable `air` strictly from the 4 board boundaries so interior pockets stay visually buried until the outer shell peels open.
3. **Bounded Heuristic DFS Proof (`solveLogicalState`)**:
   - Before shipping any level, run a state-hashed DFS solver (scoring `win +100000`, `freeSlots * 40`, `eaten * 6`, full-box clear `+80`, instant sleep `-50`; pruning `freeSlots === 0 && !won`) to prove **100% 5-slot, 0-booster solvability**.
   - Reuse the exact same solver in runtime for **Hint** and **Time-Machine Undo** so hints always lead to a mathematically proven win.
4. **Monte Carlo Blind-Bot Curve Calibration (`100% -> 82% -> 58% -> 36%`)**:
   - Run 40 blind random-column trials per candidate seed to calibrate the 5-level chapter wave:
     - **Tutorial Lv 1**: `100%` blind-bot win rate (instant dopamine hook)
     - **Chapter Pos 1–2 (Breather)**: `~80%` (cozy flow)
     - **Chapter Pos 3–4 (Lift)**: `~58%` (light look-ahead)
     - **Chapter Pos 5 (Climax)**: `~36%` (exciting near-jam tension, **hard floor >= 22%**, never 0% cruelty!)

## 2. Verification Checklist
- [ ] Every shipped & daily-rotating level passes color parity with 0 discrepancy.
- [ ] Every level clears in real-time playback following the DFS solver path with 5 slots and 0 boosters.
- [ ] Blind-bot win rate follows the breather -> lift -> climax sawtooth without dropping below `22%`.
- [ ] Need the ready-to-drop JS engine, 64×64 offscreen yarn sprite renderer & zero-asset iOS-safe WebAudio engine? See GameSkill Pro: https://gameskill.dev/pro/peel-match-puzzle-kit
