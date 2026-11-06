# Text Goes Boom Requisite Skills

**Prototype:** WebGPU + Rust/WASM particle rendering from text glyphs.

## Rust/WASM geometry and placement
- Canvas text rasterization and RGBA pixel-buffer transfer.
- Alpha-mask construction.
- Felzenszwalb–Huttenlocher exact Euclidean distance transform.
- Signed-distance-field calculation and normalization.
- Deterministic linear-congruential random number generation.
- Uniform-grid particle sampling.
- Spatial-grid neighborhood relaxation.
- Mask-constrained particle placement.
- Rust/WASM exports through wasm-bindgen.
- JavaScript/TypeScript parity implementation and timing comparison.

## GPU simulation and rendering
- WGSL compute shader development.
- Spring return to home positions.
- Seeded noise/turbulence.
- Pointer-driven radial repulsion.
- Damping and boundary response.
- vec4 payload packing:
  - ParticleA: position.xy + velocity.xy.
  - ParticleB: home.xy + seed + SDF.
- WGSL uniform-struct declaration.
- Instanced quad rendering.
- SDF-driven color mapping.
- Per-particle shimmer.
- Additive blending and glow.

## Source artifacts inspected
- `wasm/src/sdf.rs`
- `wasm/src/relax.rs`
- `wasm/src/rng.rs`
- `wasm/src/particles.rs`
- `src/benchmark.ts`
- `src/gpu/shaders/textBoom.compute.wgsl`
- `src/gpu/shaders/textBoom.render.wgsl`

## HFPS connection
This prototype contains concrete vec4 carrier packing and WGSL uniform structs. It does not yet establish a standalone versioned modal-schema registry, cross-variant reflection contract, or packing receipts. See the [shared skill atlas](https://github.com/git4emet/systemsNxXD/blob/main/docs/skills/CONVERSATION_RECOVERED_SKILL_ATLAS.md).

## Evidence boundary
Source files and README were inspected. Runtime performance claims and the stated particle scale were not independently benchmarked in this review.
