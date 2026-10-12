# Citrus / Jelly — Material Study No. 010

A self-contained interactive **WebGPU citrus soft-body study**, with no libraries or external assets.

**Live page:** https://ljq61.github.io/jelly_fruit_test/

### Features
- Drag the half-moon slice with a mouse or touch, stretch the soft attached region, and release to wobble.
- Orange, blood orange, and lemon material presets; logarithmic firmness and internal damping sliders.
- **N** nudge, **R** reset, **Space** pause/resume; optional tetrahedron mesh overlay.
- CPU Bowyer–Watson triangulation and extruded conforming tetrahedra; warm-started quaternion co-rotational shape matching, volume XPBD, and edge strain constraints.
- Fixed-step small-steps simulation, floor contact with position-based Coulomb friction, damped edges, finite-value reset.
- WGSL studio lighting, rear-face depth capture, refraction and Beer–Lambert absorption, decorative membranes/seeds/bubbles, tinted soft shadow, neutral tonemapping and sRGB dithering.
- Responsive layout and a WebGPU-unsupported screen.

### Run locally
Serve the repo using a local static server and open it in a WebGPU-compatible browser:

    python -m http.server 8080

Then visit http://localhost:8080. Alternatively, open the deployed HTTPS site. The full application is in [index.html](index.html). No build step is needed.

**Important:** This is an experimental real-time graphics material study. CPU tetrahedral simulation and WebGPU rendering are performance-dependent, particularly on mobile. Some effects are screen-space approximations (studio shadow, refractive capture, procedural inclusions), not path-traced light transport.
