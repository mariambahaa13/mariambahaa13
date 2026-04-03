# Case 1: Laminar Pipe Flow Verification (ANSYS Fluent)

## 1. Project Objective
To validate the accuracy of the ANSYS Fluent solver against the analytical Hagen-Poiseuille equations for internal laminar flow.

## 2. Analytical Design (The Physics)
Before simulating, the domain was designed using the following parameters to ensure a fully developed profile:

### A. Reynolds Number (Re)
$$Re = \frac{\rho v D}{\mu}$$
* **Density ($\rho$):** 1000 kg/m³
* **Velocity ($v$):** 0.005 m/s
* **Diameter ($D$):** 0.02 m (20mm)
* **Viscosity ($\mu$):** 0.001 Pa·s
* **Result:** $Re = 100$ (Confirmed Laminar)

### B. Hydrodynamic Entrance Length ($L_h$)
The distance required for the flow to become "Fully Developed" is calculated as:

$$L_h \approx 0.06 \cdot Re \cdot D$$

**Calculation:**
$$L_h = 0.06 \cdot 100 \cdot 0.02 = 0.12 \text{ m (120 mm)}$$

**Engineering Decision:** The domain length was set to **500 mm**. This ensures the measurement point is far beyond the $120 \text{ mm}$ entrance region, guaranteeing a fully developed parabolic profile for validation.

## 3. Mesh Quality Statistics
![Mesh Resolution](Mesh_View.png)
* **Type:** Structured Hexahedral
* **Inflation Layers:** 5 Layers at the Wall
* **Min Orthogonal Quality:** 0.78 (Excellent)
* **Max Aspect Ratio:** 2.6 (Excellent)

[Results and Plots Coming Soon]

