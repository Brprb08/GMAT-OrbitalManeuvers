# GMAT-OrbitalManeuvers

A growing set of orbital mission setups built using GMAT (General Mission Analysis Tool).  
Includes simulations of orbital transfers like Hohmann and bi-elliptic maneuvers to GEO, with visualizations, maneuver setup, and mission planning via GMAT’s Mission Sequence.

This repo is starting small as I get more familiar with the GMAT software. Right now it's focused on basic transfers using manual propagation and impulsive burns. As I learn more, I plan to add targets, solvers, and more complex mission setups for higher accuracy and realism.

---

## How to Run the Simulation

1. Open GMAT
2. Load the script file:  
   Go to `File` → `Open` and select the mission script file.
3. Run the mission:  
   Press the blue Play button. GMAT will execute the mission sequence.
4. View the plots:  
   - XYPlot windows will open automatically showing altitude over time.
   - OrbitView will display 3D orbits for both spacecraft.
5. Check the report data:  
   - Go to the **Output** tab in GMAT.
   - Click on `Hohmann_Report` and `BiElliptic_Report` to view mission data for each transfer.

---

## Notes

- All maneuvers are impulsive burns.
- No mass decrementing is used.
- Starting conditions are idealized for simplicity.
