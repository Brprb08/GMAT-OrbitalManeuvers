# GMAT Orbital Maneuvers

This repo is a growing set of orbital mission setups using GMAT (General Mission Analysis Tool).  
The goal is to get hands-on with real mission planning tools, building on earlier work with a custom Unity and C++ orbital simulator.

Instead of scripting everything from scratch, this project focuses on using a real mission design tool like GMAT to plan, propagate, and analyze spaceflight maneuvers. This includes burn sequencing, targeting, and eventually full mission flows.

---

## What this is

Right now the repo includes some starter mission scripts like:

- Hohmann transfer to GEO
- Bi elliptic transfer to GEO
- OrbitView and XYPlot visualizations
- Report data for altitude, RMAG, and velocity
- Manual impulsive burns with idealized inputs

This is the early phase. The point was to get used to GMAT’s scripting structure and mission sequence flow.

---

## Why GMAT

Before this, I built a real time orbital mechanics simulator in Unity using C++ for the physics core. That one had RK4 integration, full N body gravity, thrust vectoring, and time scaled maneuvering, all real time and GPU drawn.

But those were hand built systems. This repo is about learning how to use a real industry style tool, how to build proper missions, and how to hit constraints with tools like solvers and targeters.

GMAT is used by actual space agencies and flight engineers. Learning how to script with it, not just click around the GUI, is part of the goal.

---

## How to run the sims

1. Open GMAT  
2. Load the script file from this repo  
3. Press the blue Play button  
4. Wait for plots to show up (OrbitView and XYPlot)  
5. Check the Output tab for report files like `Hohmann_Report` and `BiElliptic_Report`

---

## In progress

Right now I’m working on a full lunar mission script that includes:

- Tanks and engine modeling  
- Mass decrementing over time  
- Solver loops with vary and achieve blocks  
- Targeting lunar orbit entry and return to LEO  
- All burns auto targeted by constraints (no hand tuning)

This will be a full LEO to LLO transfer and return.

---

## Notes

- All current burns are ideal impulsive  
- Mass is static for now (that changes soon)  
- No external forces yet (SRP, drag, third body)
