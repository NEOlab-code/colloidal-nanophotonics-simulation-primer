# Optical-data provenance for the Mie anchor (v0.2)

The tabulated subsets in this folder were transcribed from the public-domain refractiveindex.info database records listed below. Wavelength is in micrometres and the complex refractive index is written as n + i k.

- Au: P. B. Johnson and R. W. Christy, *Optical Constants of the Noble Metals*, Phys. Rev. B 6, 4370-4379 (1972), DOI 10.1103/PhysRevB.6.4370. Database record: `database/data/main/Au/nk/Johnson.yml`.
- Ag: P. B. Johnson and R. W. Christy, same reference. Database record: `database/data/main/Ag/nk/Johnson.yml`.
- crystalline Si at 300 K: M. A. Green, *Self-consistent optical parameters of intrinsic silicon at 300 K including temperature coefficients*, Sol. Energy Mater. Sol. Cells 92, 1305-1310 (2008), DOI 10.1016/j.solmat.2008.06.009. Database record: `database/data/main/Si/nk/Green-2008.yml`.
- Database descriptor: M. N. Polyanskiy, *Refractiveindex.info database of optical constants*, Sci. Data 11, 94 (2024), DOI 10.1038/s41597-023-02898-2.

For the elementary tutorial benchmark, the surrounding water is approximated as lossless and nondispersive with n = 1.333. The Mie script uses shape-preserving cubic interpolation (PCHIP) for n and k inside the tabulated wavelength interval. No extrapolation is used.

## v0.11 full Johnson--Christy tables

For the controlled NPoM surrogate, `Ag_JohnsonChristy_1972_full.csv` and `Au_JohnsonChristy_1972_full.csv` extend the previously used visible-range subsets through 1.937 micrometers using the same Johnson--Christy tabulation as the public-domain refractiveindex.info database. The calculation uses shape-preserving PCHIP interpolation without extrapolation. The manuscript separately audits interpolation of n,k and interpolation of the real and imaginary parts of epsilon; these are distinct declared numerical material constructions even though they originate from the same table.
