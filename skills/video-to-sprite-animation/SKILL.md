---
name: video-to-sprite-animation
description: Convert an AI-generated black-background action video (e.g., Seedance, Kling, Runway) into a clean, lag-free transparent sprite animation for 2D games. Covers split-zone alpha matting (preserving dark clothing/hair while keeping translucent fire/glow), foot-root anchor locking, non-linear combat timing compression with hit-stop, atlas/frame manifest packing, and first-cast texture prewarming.
---

# Video to Transparent Game Sprite Animation

Turn a selected AI action reference video into a repeatable, engine-ready transparent sprite animation where character and glowing VFX live together cleanly — without black fringes, missing dark hair/boots, floating feet, or slow-motion playback.

## 6-Step Production Pipeline

1. **Capture Clean Source**: Locked static tripod camera, pure matte black backdrop, full body + outer glow margins inside frame, record SHA-256 and `ffprobe` metadata.
2. **Split-Zone Alpha Matting (Never Global Luma!)**: Protect dark hair, clothing, and boots via a solid subject mask while deriving smooth continuous alpha from luminance strictly in the outer flame/aura zone. Apply straight-alpha color compensation `F = C / A` carefully.
3. **Common Canvas & Foot-Root Anchor Lock**: Never normalize frames by cropped alpha bounding box. Lock supporting foot to a common ground baseline and store `pivot = (rx - cx, ry - cy)` in the manifest. Premultiply RGB before downscaling RGBA.
4. **Pack with Explicit Manifest**: Export trimmed PNG frames or multi-page sprite sheets with `source_canvas`, `root_px`, `alpha_mode: "straight"`, `duration_ms`, and gameplay event indices.
5. **Non-Linear Combat Timing Compression**: Compress a sluggish `4.5s @ 24fps` AI video into a snappy `<= 1.9s` game beat with an explicit `100–140ms` Hit-Stop on the contact frame.
6. **4-Background Edge Audit & Texture Prewarm**: Inspect key frames on Black, White, Checkerboard, and real Arena backgrounds at `1.0x` and `0.25x`, and prewarm textures before first cast.
