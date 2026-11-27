---
name: card-reveal-ritual
description: Implement rarity-tiered card reveal motion and audio for deckbuilders and gacha games — 0ms instant flip for Common cards and a crisp 0.30s anticipation shake + golden light leak + rising pitch sweep + 3D flip burst for Gold Rare/UR cards. Never use flat 0ms reveals for rares or 5-second unskippable cutscenes.
---

# Rarity-Tiered Card Reveal Ritual (0.30s Anticipation Rule)

Dopamine peaks *before* receiving a rare reward — during the crisp 0.30s window where the player realizes "something big is about to drop." Treat Common and Rare reveals completely differently.

## 1. Common Cards — Zero-Latency Snap
- **Delay**: `0ms`. Total flip duration `<= 150ms`.
- Never lock input or force pauses; players must be able to rapid-flip common rewards smoothly.
- **Audio**: Short crisp paper-swoosh transient (`~80ms`).

## 2. Gold Rare / SAR / UR — The 0.30s Three-Beat Ritual
Keep the card artwork 100% untouched; create the entire emotional lift via timing, light, and sound:
1. **0.00s–0.30s (Anticipation & Light Leak)**
   - High-frequency micro-shake on the card back ramping up to `±8px`.
   - Warm golden edge light leaks through card borders while background music briefly ducks (`-6dB`).
   - Play a smooth `0.30s` upward pitch-sweep riser.
2. **0.30s (3D Flip & Burst)**
   - Snap 3D Y-flip with slight spring overshoot.
   - Trigger a soft `120ms` white-gold flash ring, `24–32` gold star sparks, and a layered low thump + major-9th arpeggio chime.
3. **0.35s+ (Holo Afterglow)**
   - Subtle 3D hover tilt + diagonal specular sweep + soft-light dark-zone rainbow shimmer.
   - Must stay skippable on click/tap without ever dropping the granted reward.

## 3. Anti-Fatigue & Accessibility Red Lines
- Total high-rarity reveal from click to interactive state must stay within **`0.8s–1.2s`** (ban >2s unskippable black-screen cutscenes).
- Respect a `Reduced Motion` toggle: keep golden border glow and audio chimes while disabling shake and full-screen flash.
