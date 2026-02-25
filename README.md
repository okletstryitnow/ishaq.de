# ishaq.de

<div align="center">

```
░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓███████▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓███████▓▒░
░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░
 ░▒▓██████▓▒░░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░░▒▓██████▓▒░
   ░▒▓█▓▒░   ░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░▒▓█▓▒░░▒▓█▓▒░      ░▒▓█▓▒░
   ░▒▓█▓▒░    ░▒▓██████▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓██████▓▒░░▒▓███████▓▒░
```

**1-file portfolio — zero dependencies, zero frameworks.**

---

</div>

## Overview

Minimal dark-theme contact page with interactive particle mesh, ASCII art header, typewriter animation, and shock effect. Single `index.html` — no build step, no bundler.

## Features

| Feature | Implementation |
|---|---|
| **Particle Mesh** | Canvas 2D — proximity-based node connections with mouse-reactive glow |
| **ASCII Art** | Block character header with auto-scaling to viewport |
| **Typewriter** | Looping typed phrases with realistic timing variance |
| **Shock Effect** | Flash overlay + shake animation on CTA hover |
| **Custom Cursor** | Dual-layer (dot + trail ring) with hover expansion |
| **Magnetic CTA** | Button follows mouse position within bounds |
| **Film Grain** | SVG noise texture overlay |
| **Scanlines** | CSS repeating gradient (CRT aesthetic) |
| **Live Clock** | Real-time CET display |

## Tech

```
Language    HTML / CSS / JS (vanilla)
Font        JetBrains Mono
Rendering   Canvas 2D + CSS animations
```

## Architecture

```
index.html
├── <style>
│   ├── CSS variables & reset
│   ├── Grain + scanline overlays
│   ├── Custom cursor system
│   ├── Content layout (flexbox, centered)
│   ├── ASCII art scaling
│   ├── Typewriter + CTA styles
│   ├── Shock keyframes
│   ├── Responsive breakpoints
│   └── Reduced motion support
├── <body>
│   ├── Cursor elements
│   ├── Shock overlay
│   ├── Particle canvas
│   ├── Vignette layer
│   ├── Content (ASCII → Name → Tagline → Divider → CTA)
│   └── Footer links
└── <script>
    ├── Particle system (spawn, update, draw, mesh)
    ├── Mouse interaction (proximity glow)
    ├── Typewriter engine
    ├── Clock
    ├── Custom cursor + smooth trail
    ├── Magnetic button
    ├── Shock effect
    ├── ASCII auto-scale
    └── Touch support
```

## Performance

No external JS. No framework overhead. Single request + one async font load.

```
Document        ~15 KB
Canvas          requestAnimationFrame
Mobile          Reduced particles, native cursor
Accessibility   prefers-reduced-motion respected
```
