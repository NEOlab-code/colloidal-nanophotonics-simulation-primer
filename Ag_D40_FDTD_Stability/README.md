# Controlled Ag dispersive-material and FDTD-ADE benchmark

Run `python scripts/fdtd_ag_d40_stability.py`. The calculation constructs a positive-strength passive Drude-Lorentz fit, compares the fitted and tabulated-data Mie spectra for a 40-nm Ag sphere, audits ADE recurrence roots, runs stable and deliberately unstable time traces, and verifies a one-dimensional dispersive Ag-film FDTD calculation against an exact transfer matrix.

The hidden 50-eV pole and wrong-sign damping cases are deliberate failure injections. The one-dimensional absorber-overlap case does not represent every PML or a surface-plasmon backward-wave geometry.
