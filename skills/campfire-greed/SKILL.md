---
name: campfire-risk-reward
description: Design high-tension roguelike Campfire / Rest Site choices using the "HP is a Currency" principle: mutually exclusive 3-way opportunity costs (Heal vs Card Upgrade vs Core Art Training) mathematically calibrated so half-HP pre-boss decisions create real tension between survival and snowballing.
---

# High-Tension Campfire / Rest Site Design ("HP Is a Currency")

Never turn rest sites into free welfare rooms that automatically heal AND upgrade. A great campfire makes players sweat between staying safe right now vs compounding power for the whole run.

## 1. Mutually Exclusive 3-Way Opportunity Cost (Pick Exactly 1)
Offer 3 options across distinct strategic axes — confirming one immediately consumes the node:
1. **Short-Term Survival (Heal)**: Restore `~25–30%` max HP (e.g., `+12` on `48` max HP). Saves *this* fight only.
2. **Single-Card Upgrade**: Upgrade one deck card (e.g., `2 -> 4` damage or lower cost).
3. **Core System Training**: Upgrade a signature finisher/art (e.g., `6 -> 8` damage, capped per art to prevent runaway scaling) that compounds every combat for the rest of the run.

## 2. Calibrate the Pre-Boss 50% HP Dilemma
- Tune the rest node right before the Region Boss so that at `~50% HP` (e.g., `24/48`):
  - **Healing** avoids sudden lethal mistakes, but extends the boss fight by `2–3` turns — risking more total damage taken.
  - **Training / Upgrading** enters the boss dangerously low, but ends the fight `~2` turns earlier and keeps compounding through future regions.
- Charge **zero gold** — the real price is forfeiting the other two choices.

## 3. Edge Cases & Safe Preview
- Clearly disable/hide an option if all eligible targets are maxed out; never waste a node.
- Backing out of an upgrade selection screen must NEVER consume the rest site.
- Keep in-run upgrades scoped strictly to the current run (isolated from permanent meta unlocks).
