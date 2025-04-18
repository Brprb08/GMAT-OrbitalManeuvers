# GMAT Orbital Maneuvers

This repo is a growing collection of orbital mission simulations using GMAT (General Mission Analysis Tool). The goal is to build out full mission flows with realistic constraints, burn sequences, and solver usage, while staying close to how real engineers would do it.

This effort follows earlier work building a real-time orbital sim in Unity with C++ physics. Here, the focus is on using professional-grade tooling instead of personally made systems.

---

## Current Scripts

### `LEO_to_LLO_Transfer.script`  
**Script:** Full Earth-to-Moon transfer and capture

This is a multi-phase mission that launches from a 400 km LEO and injects into lunar orbit using fully modeled finite burns. It features:

- Finite burn modeling with real engine performance (thrust, ISP, fuel tanks)
- Targeted Trans-Lunar Injection (TLI) using GMAT’s `DifferentialCorrector`
- Lunar Orbit Insertion (LOI) captured with solver-tuned retrograde braking
- Final near circularization to (~100 km perilune to ~300 km apilune) low lunar orbit (LLO)
- Real-time mass decrementing during burns

This is a complete, solver-driven trajectory sim, no hand tuned values for burns or coast phases. The targeting logic controls everything based on constraints like final eccentricity and altitude.

---

### `GEO_Transfer_Hohmann_BiElliptic.script`  
**Script:** Hohmann & Bi-elliptic to GEO

This script demonstrates foundational transfer maneuvers in Earth orbit using impulsive burns:

- Hohmann transfer from LEO to GEO
- Bi-elliptic transfer with apogee and perigee adjustments
- Custom burns via `ImpulsiveBurn` blocks

This one was about getting comfortable with GMAT’s basic scripting structure, maneuver sequencing, and propagation control.

---

## Why GMAT?

Before this, I built an orbital sim using RK4 integration, GPU rendering, and full multi-body gravity in Unity. But that kind of control only goes so far.

GMAT is built for real mission analysis. It lets you:

- Set up realistic spacecraft systems (mass, fuel, thrust, etc.)
- Use solvers to optimize maneuvers based on orbital constraints
- Plug into different gravity models
- Get data out, not just visuals

The goal is to grow into scripting full real world missions with accurate constraints.

---

## How to Run

1. Have GMAT installed
2. Load any `.script` script from this repo  
3. Hit the blue "Play" button  
4. Check OrbitView for visuals  
5. Open the Output tab for logs and generated reports

