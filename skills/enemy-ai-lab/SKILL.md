---
name: tactical-enemy-ai-fsm
description: Refactor monotonous AI-written enemies into tactical roguelike encounters using 4 rules: eliminate fake rest moves (0-damage openings), 100% accurate shared-formula intent telegraphs, live interruptible weaknesses (shield-break stagger / half-HP break), and visible cause-and-effect without spoiler tutorial text.
---

# 4-Layer Tactical Enemy AI & Intent Contract

AI-generated enemies frequently attack 8 turns straight — even sneaking damage into actions named `recover`. Replace random damage sponges with readable, counterable combat puzzles:

## 1. Eliminate Fake Rests (Real Counter-Attack Windows)
- Give every enemy identity 1 clear test theme (charge burst, shield counter, limited retaliation, or scaling pressure).
- Burst enemies must follow an explicit `Prep -> Burst -> Rest` cadence.
- Any action named `recover` / `rest` / `wind_down` MUST enforce `hits = 0` and `damage = 0`.
- Run an offline 8-turn audit script flagging any enemy that deals damage for 8 consecutive turns.

## 2. 100% Accurate Visible Intent Telegraphs
- Preview next turn's icon, move name, and **exact final damage/block** (including active buffs/expose/weakness).
- Intent display and actual combat resolution MUST share the exact same damage calculation function — never show `10` and hit for `14`.

## 3. Live Interruptible Weaknesses (Real-Time Intent Flip)
- Design 1 crisp counter-play hook per mechanic/elite enemy:
  - **Shield-Break Stagger**: When block drops from `> 0` to `== 0`, immediately trigger `Stagger`, crossing out the telegraphed heavy strike (`14 -> 0`) and skipping that attack.
  - **Half-HP Break**: Trigger once per battle when true HP crosses `old_hp * 2 > max_hp && new_hp * 2 <= max_hp` (immune to heal-loop farming).
- Lock resolution order strictly: `Dodge/Block/HP -> Weakness Check & Intent Refresh -> Retaliation -> Visual Snapshot`.

## 4. Visible Causality, Zero Spoiler Popups
- Ban nanny UI banners like *"Deal 3 more damage to break shield!"*.
- Communicate through unmistakable visual feedback: shield shatter VFX + enemy intent number visibly slashed to `0` + short `Staggered` badge.
