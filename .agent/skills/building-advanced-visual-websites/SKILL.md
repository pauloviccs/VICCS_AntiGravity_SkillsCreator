---
name: building-advanced-visual-websites
description: Designs, plans, and validates high-performance websites with complex visual components such as 3D rendering, GPU-accelerated animations, shader-based effects, and Liquid Glass–style interfaces. Use when the user mentions WebGPU, Three.js, advanced UI effects, interactive portfolios, creative web experiences, or performance-critical visual simulations.
---

# Building Advanced Visual Websites

## When to use this skill
- The user requests websites with **3D graphics, shaders, or simulations**
- The user mentions **WebGPU, WebGL, Three.js, Babylon.js, or R3F**
- The user wants **Liquid Glass / glassmorphism / refraction effects**
- The project requires **high visual fidelity with strong performance**
- The site is a **portfolio, experimental website, or creative showcase**

---

## Workflow

### Checklist
- [ ] Identify visual complexity level (UI-only / 3D / simulation)
- [ ] Choose rendering pipeline (CSS / WebGL / WebGPU)
- [ ] Select animation system (timeline vs physics-based)
- [ ] Define performance constraints (mobile, desktop, GPU load)
- [ ] Validate browser compatibility
- [ ] Apply progressive enhancement strategy

---

## Plan → Validate → Execute Loop

### Plan
- Define which parts are **GPU-bound** vs **CPU-bound**
- Decide whether visuals are **decorative or interactive**
- Choose fallback strategies for low-end devices

### Validate
- Confirm WebGPU availability before enabling heavy effects
- Measure frame stability (target: 60 FPS)
- Verify memory usage and shader complexity

### Execute
- Implement visuals incrementally
- Optimize before adding new effects
- Lock visuals behind feature detection

---

## Core Technology Stack (2026)

### Rendering & Simulation
- **WebGPU**
  - Primary choice for advanced shaders, refraction, fluid simulation
  - Enables compute shaders and modern GPU pipelines
- **Three.js (WebGPU renderer preferred)**
  - Scene graph, materials, loaders, post-processing
- **React Three Fiber**
  - Declarative scene composition in React-based projects
- **Babylon.js**
  - Use for simulation-heavy or game-like environments

---

### Animation & Interaction
- **GSAP**
  - Timeline-based animations
  - Scroll-driven storytelling
- **Physics / Simulation**
  - GPU particles via compute shaders
  - WASM modules for math-heavy logic

---

### Liquid Glass–Style Effects

#### Lightweight UI Glass
- CSS `backdrop-filter`
- SVG filters:
  - `feGaussianBlur`
  - `feDisplacementMap`
- Use only for:
  - Panels
  - HUD elements
  - Navigation layers

#### Physically Accurate Glass
- Fragment shaders using:
  - Refraction vectors
  - Normal maps
  - Environment sampling
- Requires:
  - WebGL (advanced)
  - WebGPU (preferred)

---

## Performance Rules

### Mandatory
- Use **requestAnimationFrame**
- Throttle animations when tab is inactive
- Dispose GPU resources explicitly
- Avoid overdraw in shaders

### Optimization Strategy
- Prefer **compute shaders** over JS loops
- Offload math-heavy logic to **WebAssembly**
- Use LOD (Level of Detail) for 3D assets
- Defer non-critical visuals

---

## Frontend Architecture

### Recommended Frameworks
- **Astro**
  - Content-heavy sites with isolated interactive islands
- **Next.js**
  - React + SEO + R3F integration
- **SvelteKit**
  - When minimal JS and performance are critical

---

## Progressive Enhancement Strategy

- Detect:
  - WebGPU → Enable full visuals
  - WebGL → Enable reduced visuals
  - No GPU features → Static UI fallback
- Never block content behind visuals

---

## Error Handling

- If unsure about shader behavior:
  - Run validation builds
  - Reduce shader complexity
- If performance drops:
  - Disable post-processing first
- For scripts:
  - Run with `--help` before execution

---

## Resources
- `/scripts/` – GPU capability detection helpers
- `/examples/` – Reference scenes (3D, glass, shaders)
- `/resources/` – Shader templates and UI overlays
