# Inflammation-and-Cardiovascular-Dynamics
Inflammation and Cardiovascular Dynamics

Matlab Files

This repository contains files to run results published in Journal of Physiology. Code reproduces results in Figures 7 (simulations with mean data from the Janum study and the Copeland study) and Figures 8 and 9 (displaying results of various treatments).

This repository consists of two folders for 1) solving the model (RunModel) and 2) studying the impact of treatments (Treatments).
Running the model DriverBasic.m Solves the odes with either nominal or optimized parameter values

Files in "RunModel": 
- DataCopeland.mat and DataJanum.mat includes values for all the cytokine measurements, blood pressure, heart rate, pain, and temperature. 
- RunCopeland.m and RunJanum.m solves the differential equations for each parameter set and plots the solution (Figure 7a and b)
- load_pars_Init_Copeland.m and load_pars_Init_Janum.m loads all parameters (optimized parameters), the files also list nominal parameter values
- modelDriver.m a wrapper that sets the integration tolerance and calls Matlab's delay differential equations solver dde23
- model.m the right hand side of the differential equations.

Files in "Treatment": 
- Treatments.m runs all the treatments for results shown in Figure 8 (single treatments) use lines 22-32 and 
  for results with combination treatments shown in Figure 9 use lines 34-47.
- load_pars_Init.m load parameters and initial values used for treatment simulations
- modelDriver.m a wrapper that sets the integration tolerance and calls Matlab's delay differential equations solver dde23
- model.m the right hand side of the differential equations.
- SustEndotox.m function used to generate sustained endotoxemia
- TransEndotox.m function used to generate transient endotoxemia
- TreatXXX.m the code used to generate the individual treatments with Antipyretics, Vasopressors, and LPS adsorption
