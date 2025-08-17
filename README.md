# Heat Sink Thermal Conduction Analysis – ANSYS Fluent

##  Project Overview
This project focuses on the **thermal analysis of a circuit board heat sink** using ANSYS Fluent.  
The study models heat conduction within the solid fins and accounts for heat exchange with the environment through boundary conditions, without explicitly solving the fluid flow domain.  

The objective is to evaluate the **temperature distribution within the heat sink** under steady-state conditions, considering realistic processor heating and air convection.

##  Geometry & Model Setup
- Modeled **half of a circuit board heat sink** (symmetry used to reduce computational cost).
- **Dimensions:**
  - Fin thickness: 1 mm  
  - Fin height: 19 mm  
  - Gap width: 2 mm  
  - Fin length: 30 mm  
  - Number of fins: 5  
- Only the **solid domain** is modeled to focus on heat conduction.

##  Boundary Conditions
- **Wall-Sink-Base:** Constant temperature at **350 K** (processor heat source).  
- **Wall-Sink-Air:** Convective condition with a **heat transfer coefficient of 32 W/(m²·K)** and ambient air temperature of **290 K**.  
- **Symmetry Plane:** Symmetry condition applied to exploit model symmetry.  
- Only the **energy equation** is solved, as no fluid regions are included.


##  Simulation Details
- **Solver:** Pressure-based, steady-state.  
- **Physics:** Heat conduction in solid domain + convection via boundary conditions.  
- **Assumptions:**  
  - No fluid region modeled (convection treated as boundary condition).  
  - Material assumed to be solid metal.  

## Results
- Steady-state temperature distribution within the heat sink fins.  
- Identification of thermal gradients from the base (processor) to the fin tips.  
- Insights into effectiveness of heat dissipation through conduction and convection.
