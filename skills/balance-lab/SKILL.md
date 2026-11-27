---
name: roguelike-balance-pacing
description: Tune roguelike difficulty curves without breaking weak archetypes using 4 rules: 100+ seeded headless baseline simulations first, ban global +ATK reverse pressure, tune normal-fight PACING_HP multipliers (1.0 -> 1.1 -> 1.3), and isolate scope by locking elites, bosses, and economy.
---

# 4-Rule Roguelike Numerical Balance Protocol

Never tune mid/late-game difficulty by guessing or adding global `+1 ATK` to enemies. Follow this evidence-first 4-step workflow:

## 1. Run a Seeded Headless Baseline First (100+ Runs)
- Write a headless CLI simulation script supporting `--seeds=a-b` and feature flags (`--pacing=0|1`) across every character × strategy.
- Log per-character, per-region metrics: win rate, average HP loss per normal fight, HP entering boss, and gold earned/spent.
- Catch structural bugs first (e.g., Region 3 accidentally easier than Region 2).

## 2. Ban "Reverse Pressure" (Global `+ATK` Trap)
- Compare every tuning candidate on the **exact same seeds** against baseline.
- Global `+1 Enemy ATK` multiplies by turn count: a 2-turn aggro build barely notices (`+2 dmg`), while an 8-turn defensive/slow build takes `+8 dmg` per fight and collapses.
- Prefer **staged normal-fight HP multipliers (`PACING_HP`)** so fast decks spend half a turn more and slow decks stay viable.

## 3. Strict Single-Variable Scope Lock
- Change ONE variable per tuning batch — for example, scale only normal-fight HP by fights completed in the region (`1–2 -> 1.0x`, `3–4 -> 1.1x`, `5+ -> 1.3x`).
- Keep Elites, Bosses, enemy ATK, intents, and shop prices **locked** when baseline data for them is healthy.
- Gate new pacing rules to new runs so existing saves stay backward-compatible.

## 4. Delivery Evidence
- Deliver a same-seed comparison table (Baseline vs Candidate A/B) plus automated unit tests covering tier boundaries, locked elite/boss values, and save compatibility.
