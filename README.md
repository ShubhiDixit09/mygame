# ME VS ME

**Your next connection could be your last.**

A complete browser game built for Neural Nash — IGTS × OpenAI Student Collective at DTU. Revives the pencil-and-paper game **Sim** as an atmospheric orbital duel.

## Play

Choose two of six beacons to claim a connection. Players alternate. Complete a triangle in your own colour and **you lose**. Crossing connections do not form additional vertices. With six points, every complete two-colouring contains a monochromatic triangle: a draw is impossible.

- **VS MACHINE**: play a local tactical computer opponent (bounded minimax with alpha-beta pruning; not an LLM).
- **LOCAL 1V1**: two players, one device, alternating turns.
- Click or tap two beacons, or use keys **1–6**. **Escape** cancels a selection.
- Hover previews fatal connections. Toggle the original generative synth soundtrack in the header: evolving chords, stereo arpeggios, delay/reverb, pulse percussion and reactive sound effects. Audio is synthesized locally with Web Audio; no recordings or external samples.
- Match scores persist per mode in browser localStorage.

## Visual system

Custom Canvas 2D renderer produces dimensional chrome spheres, orbital ribbons, animated cables, gravity well, pointer parallax, motes and collapse particles. Acid green, rose and violet; oversized editorial typography. Responsive layout, native dialogs, labelled keyboard-accessible beacon controls, reduced-motion support. No image assets or game runtime dependencies. Google Fonts are optional; system fallbacks are supplied.

## Run / deploy

Serve `dist/` with any static host, e.g. `python3 -m http.server 8000 --directory dist`. There is no build step. Set the hosting output directory to `dist` for Cloudflare Pages, Netlify or Vercel.

`npm test` runs the rules/AI tests, all 32,768 complete colourings of K6, and 100 simulated matches.

## Scope

Local 1v1 and computer play are implemented. Online networked multiplayer is not included. Visuals use Canvas projection/shading, not a WebGL engine. Computer play is bounded search and is not guaranteed optimal.
