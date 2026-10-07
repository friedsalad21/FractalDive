# FractalDive

**▶ Open it live: https://friedsalad21.github.io/FractalDive/**

A fast GPU fractal explorer for the Mandelbrot set, Burning Ship, Tricorn and Multibrot (powers 3–5), plus the Julia set of any point. Zoom in a very long way, down to about 10⁻⁶⁶, and the image stays sharp. A WebGL shader uses perturbation theory: one high-precision reference orbit is worked out with BigInt in a Web Worker, and every pixel is computed on the GPU as a small offset from it, with rebasing to avoid glitches. The iteration count goes up by itself as you zoom deeper, and you can set it by hand.

- Scroll to zoom toward the cursor, drag to pan, double-click to zoom in (shift: out), pinch and drag on phones, plus zoom and reset buttons
- Smooth colouring with no banding, 12 palettes, offset and density sliders, and optional slow colour cycling
- Julia preview: hover over the fractal to see the Julia set for that point, then click to explore it full screen
- Every view lives in the URL: type, centre (as long decimal strings, so deep spots survive), zoom, iterations and colours. "Copy link" shares the exact spot
- Famous spots: Seahorse Valley, Elephant Valley, a mini-Mandelbrot, a spiral, two deep mini-Mandelbrots (10⁻¹⁵ and 10⁻³²), the Burning Ship armada and a spiral Julia set
- Save a PNG at screen size, 2× or 4× (rendered in tiles, good for wallpapers)
- Dive: an animated zoom from the full view into the current spot
- Keys: arrows pan, `+`/`-` zoom, `P` palette, `J` Julia, `D` dive, `C` copy link, `R` reset, `H` panel

Single `index.html`, no build step and no libraries: open it in a browser that supports WebGL 2. Open `index.html?test` to run the self-check of the URL encode/decode round trip, which includes a 40-digit centre.
