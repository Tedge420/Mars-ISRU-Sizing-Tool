# Mars ISRU Propellant Plant Sizing Tool
 
A MATLAB sizing tool for evaluating the feasibility of In-Situ Resource Utilisation (ISRU) propellant production on Mars. Developed as part of an undergraduate dissertation at the University of Manchester (2026).
 
## What it does
 
The tool calculates the mass, power, and energy requirements of a Martian LOX/CH4 propellant plant using the Sabatier process and water electrolysis. It evaluates three candidate power architectures (solar with battery storage, Kilopower nuclear fission, and RTG) and outputs a full subsystem mass breakdown and total landed mass for each.
 
## Requirements
 
- MATLAB (any recent version)
## How to use
 
1. Open the .m file in MATLAB
2. Go to the **USER INPUTS** section at the top of the script
3. Select your mode:
   - **Mode 1** — enter a propellant target (kg) and mission duration (days) → tool calculates required continuous power
   - **Mode 2** — enter available power (kW) and mission duration (days) → tool calculates maximum propellant output
4. Adjust any other inputs as needed (O/F ratio, efficiency parameters, storage tanks)
5. Run the script
## Outputs
 
- Console report with mass balance, energy budget, subsystem masses, and total landed mass for all three power architectures
- Figure 1: Propellant mass balance pie chart
- Figure 2: Energy budget showing gross demand vs thermal recovery
- Figure 3: Total landed mass comparison across all three power architectures
## Methodology
 
All equations, assumptions, and baseline values are documented in:
 
> Lungu, M. (2026). *A Feasibility Study and Trade-off Analysis of In-Situ Resource Utilisation for Interplanetary Missions*. Unpublished BEng dissertation, Department of Mechanical and Aerospace Engineering, University of Manchester.
 
The subsystem baseline masses are derived from Kleinhenz & Paz (2017) and scaled using a throughput ratio relative to the baseline mission of 30,000 kg propellant over 510 days.
 
## Notes
 
- Storage tanks can be toggled on or off using the `include_storage` flag depending on whether the MAV is co-located with the plant
- All Martian environmental constants (irradiance, dust degradation, diurnal cycle) are hardcoded based on values from the literature
- The tool is intended as a first-order feasibility assessment and should be used alongside the full methodology documented in the dissertation
 
