# Method and limitations: Ag_D40_FDTD_Stability

## Purpose

This controlled calculation is motivated by the 40 nm Ag sphere case in the source tutorial, which reports a finite frequency-domain response but a field blow-up in one MEEP calculation. The original input file and numerical settings are unavailable. This archive therefore does not reconstruct that run; it separates possible causes with independently reproducible tests.

## Components

1. Johnson--Christy Ag data over 300--700 nm are represented by a constrained positive-strength Drude plus four-Lorentz model.
2. Exact Mie theory compares the tabulated and fitted material responses for a 40 nm Ag sphere in lossless water.
3. The centered ADE recurrence is audited by its characteristic-root spectral radius.
4. Wrong-sign damping and an artificial weak 50 eV pole are deliberate failure injections.
5. A one-dimensional 40 nm Ag film is propagated by FDTD--ADE and compared with an exact transfer-matrix solution using the same material fit.
6. Spatial-grid and Courant-factor sweeps separate interface discretization from stable time-step sensitivity.
7. A one-dimensional matched electric/magnetic conductivity absorber is tested with a dispersive half-space extending into it.

## Important limitations

- The sphere response is exact Mie theory, not a three-dimensional FDTD sphere rerun.
- The propagation benchmark is one dimensional and normally incident.
- The simple matched conductivity absorber is not a universal PML test.
- The model contains no surface-plasmon backward-wave channel.
- Absorption in the FDTD spectrum is inferred as `1-R-T` and is not an independent energy-conservation observable.
- The hidden 50 eV pole is a diagnostic stressor and is not part of the fitted silver model.
- The passive pole fit is one educational constrained fit, not a unique global parameterization of silver.
