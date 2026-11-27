---
name: buttonless-card-hand-ux
description: Build jitter-free, buttonless 2D card hand interactions (4-layer contract + 3-step UI subtraction): zero neighbor displacement on hover, zero blocking hover tooltips, disjoint hover strips, and drag-past-threshold casting with safe cancel zones. Use whenever AI-built card hands jitter, push neighbors, or clutter the screen with confirm buttons.
---

# 4-Layer Buttonless Card Hand & UI Subtraction Contract

AI-generated card hands almost always push neighboring cards sideways on hover, spawn giant black tooltips covering enemies, and bolt ugly Confirm/Cancel buttons underneath. Fix it with 4 strict layers and 3 UI subtraction rules.

## Part A — 3-Step UI Subtraction Formula (Works for Any Game UI)
1. **Lock the Anchor**: Keep the player's eyes and pointer strictly inside the primary play zone.
2. **Ban Extra Chrome**: Explicitly forbid new standalone buttons, modal popups, or floating external slots.
3. **Reuse Existing Gestures**: Bind new actions to existing drag-up, drag-down, hold, or right-click gestures.

## Part B — 4 Mandatory Card Hand Layers
1. **Layer 01 — Zero Neighbor Displacement (`neighbour_dx < 0.5px`)**
   - Hovering a card must NEVER push left/right neighbors sideways (which causes misclicks).
   - Lift and straighten ONLY the hovered card (`rotation -> 0`, `scale -> 1.15x`, top z-index) over `0.12s`.
2. **Layer 02 — Delete Blocking Hover Tooltips (`CardTooltip == 0`)**
   - Remove giant black hover boxes that cover enemies. Force concise single-sentence card text directly on the card face.
3. **Layer 03 — Disjoint Narrow Hit Strips (`hover_strip`)**
   - Overlapping card borders cause rapid focus flicker when sweeping the pointer horizontally.
   - Assign each card an exclusive non-overlapping hit rectangle; sweeping left-to-right must monotonically visit `0 -> 1 -> 2 -> 3 -> 4` with zero flicker.
4. **Layer 04 — Threshold Drag Cast & Safe Cancel**
   - Hover/click only inspects; **dragging upward past `PLAY_LINE_Y` and releasing** casts immediately (drawing a bezier aim arc for targeted cards) with zero Confirm button.
   - Short drag, diagonal fumble, dragging back down, leaving window, or pressing `Esc` cleanly cancels with zero accidental casts.
