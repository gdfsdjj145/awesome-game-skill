---
name: sar-holo-card-shader
description: Upgrade any existing 2D game card artwork into a 3D tilting SAR holographic foil card purely via code (3-mask preprocessing + 8-layer metallic edge thickness + soft-light dark-zone rainbow diffraction + Sobel ink emboss + sweep-synced 4-point star flares). Never redraw original card art with generative AI.
---

# Code-Driven SAR Holographic Foil Card Shader

Upgrade flat game cards into collectible SAR/UR holographic cards purely in code — **100% preserving original artwork without AI redrawing**.

## 1. One-Time Preprocessing (3 Luminance/Edge Masks)
Compute three masks once per card artwork:
- **Dark-Zone Mask**: Where holographic rainbow foil lives. **Critical**: clamp out pure-black ink lines and dark hair so they never turn neon green.
- **Bright-Zone Mask**: Drives angle-dependent hot gold/silver metallic reflections.
- **Sobel Edge Map**: Lighten edges facing the virtual light and darken opposite edges for subtle printed-ink emboss.
- Extract dominant saturated accent color + 4–5 well-spaced highlight anchors for star flares.

## 2. 3D Card Body & Physical Thickness
- Orbit tilt smoothly (`±17°` horizontal Y, `±10°` vertical X) driven by pointer/gyroscope or seamless sin/cos loop.
- Stack **8 brushed-metal slices** behind the card face to create tangible edge thickness + rotating metallic bevel edge (gold / ice silver / crimson / prismatic).
- Shift drop shadow opposite the tilt angle against a dark vignette tinted by the card's dominant hue.

## 3. Zoned Holographic Shading (No Burned Faces)
- **Dark zone**: Fine base pattern (sunburst / silk wave / cosmos) + micro-grating + two counter-moving rainbow diffraction layers blended with **`soft-light`** (ban `color-dodge`, which scorches faces and dark areas into neon sludge).
- **Full card**: Diagonal specular sweep band + pointer-tracking soft spotlight.
- **Star flares & particles**: 4-point cross flares at highlight anchors peak as the sweep passes; add slow background + foreground drifting particles in the card's accent hue.
