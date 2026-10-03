# SKILL: web3d-gpu

**Gives the agent:** browser games and immersive 3D product UIs — WebGL/WebGPU rendering, game
loops, physics/economy systems, and 3D "signature" interfaces.
**Sources:** Tidewater ($30K, 82K LOC) · WaterCuda ($20K, C++/WASM kernels) · win12/W12 desktop
simulators ($6.5K/7K) · 3DMIND/3dspace ($7.5K/6K) · SenP neural brain ($8K) · FISHKAL Deep Catch ·
Fable Berger · ImX 3D Landing · AI Skills & Demos (13 playable demos).

## When to use
- Browser game with world/economy (fishing, sims, arenas).
- Product page or dashboard with a Three.js/WebGPU hero.
- Desktop/OS-simulator interfaces with windows, HUDs, live telemetry.

## Core capabilities
1. **Engine layer (small, owned)**: renderer setup, camera controls, entity/component basics,
   tick loop with fixed-step physics + variable render (Tidewater pattern); asset manifest + LOD.
2. **WebGL craft**: instancing for crowds/vegetation, texture atlases, frustum culling, budgeted
   shadows; graceful `webgl2` fallback screens.
3. **WebGPU/WGSL path**: small compute pipelines for particles/water (Law L7: studied tidewater,
   then built own `packages/webgpu-mini` in the roadmap manifest).
4. **C++/WASM kernels**: performance-critical simulation compiled to WASM with JS shims
   (WaterCuda pattern: compile → memory handle → typed-array views).
5. **Game systems**: save/load (versioned localStorage), economy with price tickers, upgrades,
   day/night + weather state machines.
6. **Signature 3D UI**: particle identity scenes, neural-brain node graphs, holographic panels —
   dark neon palette (#06060e bg, cyan/purple/gold accents), mono HUD labels.
7. **Desktop simulators**: window manager (drag/resize/z-order), taskbar/start menu, boot sequences,
   per-app state — Next.js static-export or Vite single-file.

## Workflows
- **Hero scene:** art direction → particles/gradient mesh → mouse parallax → perf budget (60fps mid-tier).
- **Game slice:** core loop (cast→fight→sell→upgrade) → placeholder art → economy tuning → polish.
- **Signature UI:** 3D visualization must answer a real question (tokens, agents, state) — decoration alone is rejected.

## Quality bar
- 60fps on mid-tier laptop; FPS counter in dev builds; assets lazy + compressed.
- `prefers-reduced-motion` respected; mobile touch fallbacks.
- Scene teardown tested (no leaked contexts/listeners on route change).

## Price anchor
Single 3D page $2.5–5K · Vite 3D app $5.5–9K · Full game $18–30K (+GPU engine $8K) → `PRICING.md` §5.
