---
name: positive-relic-design
description: Cure the AI "poison contract" anti-pattern in roguelike relic/item design — build purely positive, exciting power-ups and prevent infinite loops via deterministic trigger-priority queues and per-turn caps instead of tacked-on negative penalties.
---

# Positive Relic Design & Ordered Trigger Queues

When asked to design boss relics or rare items, LLMs suffer from a classic cliché: attaching annoying downsides to every reward (*"Draw 1, BUT lose all resources at end of turn"*). Fix it at the workflow level.

## 1. Core Principle: Relics Should Empower, Not Punish
- Explicitly forbid AI agents from treating "missing downside" as a design flaw.
- Rewrite poison contracts into clean positive identities:
  - Instead of *"First attack -1 cost, all other attacks +1 cost"* -> *"First eligible attack each turn costs -1."*
  - Instead of *"Draw 1 on finisher, wipe stored resources"* -> *"Draw 2 on finisher; keep all resources."*

## 2. Prevent Infinite Loops Without Downsides
Control power ceilings through **structure and ordering**, not feel-bad penalties:
1. **Deterministic Priority Queue**: When multiple cost-reduction relics apply (e.g., `Relic A -> Relic B -> Relic C`), evaluate them in a fixed 1-2-3 order. If `A` and `B` already reduce a card to `0` cost, `C` does NOT waste its trigger — it stays saved for the next eligible card.
2. **Explicit Per-Turn / Per-Combat Caps**: Bound draw/energy refund loops with crisp finite counters rather than awkward punishments.
3. **Automated Loop & Window Testing**: Run automated single-turn stress windows verifying zero unintended infinite recursion across all relic combinations before shipping.
