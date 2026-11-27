---
name: roguelike-map-topology
description: Build a 4-layer Roguelike Map Generator that eliminates fake choices (0% row-1 start merging, 7-lane cross-region planar walks with zero edge crossings, >=55% two-exit branching rate, and mandatory safe bypass paths before every Elite node).
---

# 4-Layer Roguelike Map Generator (Real Choices, Not Linear Corridors)

Naive random map generators create 4 start nodes that immediately merge on row 1, disconnect left/right halves, and trap players in single-lane corridors. Enforce these 4 graph & pacing layers:

## 1. Layer 01 — Independent Starts (`row1_merge == 0%`)
- Track `owner[row1_node] = start_index`. Different start nodes must NEVER share a Row-1 destination.
- Guarantee every starting path encounters at least one meaningful branch (e.g., Combat vs Event) within its first 3 steps.

## 2. Layer 02 — Cross-Region Planar Walks (`crossings == 0`)
- Run 6 random walks (`delta in {-1, 0, +1}`) across 7 logical lanes so left and right regions naturally bridge together.
- Reject any candidate edge `(a -> b)` that crosses an existing edge `(e0 -> e1)` on the same row:
  `(a - e0) * (b - e1) < 0` -> reject immediately.

## 3. Layer 03 — Hard Branching Floor (`TARGET_TWO_EXIT >= 0.55`)
- After primary walks, scan single-exit nodes and grow valid planar side branches (`branch_walk()`) until **at least 55%** of branchable nodes offer `>= 2` exits.

## 4. Layer 04 — Pacing & Elite Safety Valves
- **Mandatory Elite Bypass**: Every parent of an Elite node must have `next.size() >= 2` so low-HP players can always route around an Elite while healthy players can greed for relics.
- **No Back-to-Back Specials**: Elite, Shop, and Rest nodes must never connect directly to the same special type.
- **Combat Streak Cap**: Limit consecutive regular combats to `<= 3`.

## Verification Checklist
- Run 1,000 seeded map generations and assert: `row1_merge == 0`, `crossings == 0`, `two_exit_rate >= 0.55`, `elite_without_bypass == 0`.
