# Tethered Electric Aircraft (Design, Build & Test)

**University of Sheffield | Module: ELE101 / AER11002 (Group 56)**  
A complete engineering cycle for a tethered electric aircraft designed for circular flight. The project encompassed aerodynamic sizing, hybrid balsa/composite airframe manufacturing, bench power telemetry analysis, and pitch-stability aerodynamic redesign.

---

## Technical Specifications
* **Wingspan & Chord:** 500 mm span, 82 mm chord (Aspect Ratio = 6.1)
* **Aerofoil Profile:** NACA 2412 with 4° incidence and 10° dihedral angle for sideslip stability
* **Fuselage Length:** 284.2 mm (Optimized using Zaic ideal fuselage length criteria)
* **Airframe Materials:** Laser-cut balsa ribs, 3D-printed root/tip impact ribs, 3-layer balsa/plywood sandwich fuselage
* **Main Spar:** 4 mm hollow carbon fiber tube serving as the wing structural spar and tether line pass-through
* **Propulsion:** Single nose-mounted electric motor in puller configuration

---

## Aerodynamic Performance & Flight Testing

Flight data was captured during tethered flight testing using a bench power supply set to a constant 13.0V. 

| Parameter | Takeoff / Acceleration | Steady Cruise | Notes |
| :--- | :--- | :--- | :--- |
| **Current Draw** | 3.2 A | 2.1 A | Drop indicates transition to level cruise |
| **Electrical Power ($P = IV$)** | 41.6 W | 27.3 W | Supplied via bench power unit |
| **True Airspeed (TAS)** | — | 5.88 m/s | Derived from 24.4 RPM tether angular velocity |
| **Estimated Lift / Drag** | — | $L \approx 1.47\text{ N}$, $D \approx 0.67\text{ N}$ | $L/D \approx 2.2$ at cruise |
| **Total Propulsive Efficiency** | — | **14.4%** | Combined motor electrical loss & low-Re prop efficiency |

---

## Engineering Iteration: Pitch Stability Analysis

During the initial flight test, the aircraft experienced low-speed pitch instability and pilot-induced oscillations, leading to a crash landing. 

### Root Cause & Redesign:
1. **Defect:** The original horizontal stabilizer was undersized and located in the wing's downwash zone, causing poor control authority at low speeds.
2. **Aerodynamic Sizing:** Applied the Tail Volume Coefficient formula ($S_t = \frac{V_t \cdot S \cdot c}{l_t}$) to calculate the exact required tail surface area ($S_t$) relative to wing area ($S$), mean aerodynamic chord ($c$), and tail moment arm ($l_t$).
3. **Outcome:** Manufactured a larger, mathematically optimized parallelogram tailplane and converted the assembly to a T-tail layout to clear wing downwash. Subsequent flight tests confirmed full pitch stabilization without low-speed oscillation.

---

## Repository Contents
* `/documentation/` - Final Design Report, Flight Test Performance Report, and Project Gantt Chart.
* `/cad/` - STEP files for airframe, sandwich fuselage layers, and optimized tailplane.
* `/media/` - Photos of flight testing and CAD section views.
