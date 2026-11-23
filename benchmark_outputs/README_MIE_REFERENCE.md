# Mie-anchored single-particle benchmark (v0.3)

This folder contains analytic references for five homogeneous-sphere benchmark cases. The reference does **not** reproduce or validate FEM, FDTD, FIT, or SIE outputs by itself; those numerical runs require original solver files or complete rebuild specifications and independent convergence sweeps.

## Assumptions

- Lossless nondispersive water, n = 1.333.
- Au and Ag: Johnson-Christy 1972 tabulated n,k, PCHIP interpolation.
- Si: Green 2008 tabulated n,k at 300 K, PCHIP interpolation.
- Vacuum-wavelength grid: 1 nm.
- Cross sections are calculated from the exact homogeneous-sphere Mie coefficients.

## Peak summary

| case    | material   |   diameter_nm |   extinction_peak_wavelength_nm |   extinction_peak_nm2 |   scattering_peak_wavelength_nm |   scattering_peak_nm2 |   absorption_peak_wavelength_nm |   absorption_peak_nm2 |   max_scattering_fraction |   max_nmax |   max_energy_balance_abs_nm2 |
|:--------|:-----------|--------------:|--------------------------------:|----------------------:|--------------------------------:|----------------------:|--------------------------------:|----------------------:|--------------------------:|-----------:|-----------------------------:|
| Au_D100 | Au         |           100 |                             570 |         54902         |                             578 |        37385          |                             543 |               21017   |                   0.87894 |          8 |                   7.276e-12  |
| Au_D40  | Au         |            40 |                             527 |          3829.2       |                             536 |          268.4        |                             526 |                3583.1 |                   0.34516 |          6 |                   4.5475e-13 |
| Ag_D40  | Ag         |            40 |                             399 |         26372         |                             399 |        16276          |                             399 |               10096   |                   0.71421 |          6 |                   1.819e-12  |
| Ag_D100 | Ag         |           100 |                             389 |         67195         |                             480 |        55172          |                             388 |               17695   |                   0.97081 |          8 |                   7.276e-12  |
| Si_D150 | Si         |           150 |                             613 |             1.341e+05 |                             613 |            1.2769e+05 |                             480 |               33037   |                   0.98814 |          9 |                   1.6371e-11 |

## Required next comparison

For every retained numerical solver, export spectra on the same wavelength grid and report maximum and RMS relative errors versus `mie_reference_all_cases.csv`, together with mesh/grid/time/PML convergence, wall time, peak memory, software version, and hardware.
