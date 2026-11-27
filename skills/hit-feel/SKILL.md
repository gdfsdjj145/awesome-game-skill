---
name: hit-feel-5-layers
description: Add crisp 5-layer combat hit feel to any 2D game (Distance Bridge, Hit-Stop, 2-Frame Pure White Flash + 4-Frame Tint, Front Impact Core + Squash/Knockback, and ±18px Staggered Damage Numbers + 3-Band Layered SFX). Use whenever AI-generated attacks feel floaty, weak, or like hitting air.
---

# 5-Layer Combat Hit Feel Contract

When you ask an AI to "add hit feel", it usually flashes the target weakly and runs `hp -= damage`. Real combat impact is **not one effect** — it is **5 synchronized layers** firing in the exact right millisecond window.

## The 5 Mandatory Layers

1. **Layer 01 — Distance Bridge (No Hitting Air)**: Every attack must physically close the gap before impact — melee lunges to contact (`gap -> 0px`) or spawns a visible projectile/wave entity that triggers impact strictly on arrival.
2. **Layer 02 — Hit-Stop (Impact Freeze)**: Freeze motion at the exact frame of contact: Light `83ms`, Medium `100ms`, Heavy `133ms`, Ultimate `150ms`. Restore time scale safely on scene abort.
3. **Layer 03 — Crisp Hit Flash (2f Pure White + 4f Accent Tint)**: Ban muddy 170ms pale ghosts. Render 2 frames (`33ms`) of 100% pure white silhouette followed by 4 frames (`67ms`) of hot accent tint.
4. **Layer 04 — Front Impact Core + Squash & Knockback**: Draw a white-hot core **in front of the target's torso** for 3 frames, squash (`0.90x / 1.08y`), knock back `15–90px` with spring recovery, plus micro camera shake and dust burst.
5. **Layer 05 — Staggered Damage Numbers + 3-Band Layered SFX**: Offset multi-hit popups by `±18px` (never overlap `2+2 -> 22`) and layer Low sub-bass thump + Mid crack + High wind transient.

## Verification Checklist
- [ ] Distance gap reaches `0px` (body or projectile) on the exact frame damage triggers.
- [ ] Triggering a 3-hit combo displays 3 clearly legible, non-overlapping damage popups.
- [ ] Toggling `Reduced Motion` or aborting mid-animation restores positions, tint, and time scale to `1.0`.
