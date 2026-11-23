# JAP26-TU-04279 Revision Data and Code Archive v2.0.0

This archive supports the revised Tutorial **“A Primer on Electromagnetic Numerical Simulation for Colloidal Nanophotonics”** by Jaewon Lee and Seungwoo Lee, submitted to the *Journal of Applied Physics*.

## Scope

The archive contains input optical constants, scripts, convergence series, tabulated outputs, figures, dependency records, method limitations, and execution notes used for the manuscript’s pedagogical benchmarks. It includes the revision-specific additions requested by the reviewers:

1. a complete three-dimensional voxel-DDA sphere benchmark;
2. a self-consistent layered-dipole substrate comparison;
3. extended Au-trimer multipole truncation through `lmax = 16`;
4. extended NPoM multipole truncation through `lmax = 16` and MFS source-placement/off-collocation residual tests.

## Directory map

- `scripts/`: Python calculation and figure-generation scripts.
- `data/`: compact source and output tables used directly in revised figures and tables.
- `benchmark_outputs/`: analytic Mie reference tables.
- `reproducibility/`: standalone benchmark records, full convergence files, execution notes, and explicit limitations.
- `figures/`: numerical figure outputs in PDF/PNG/SVG formats and original vector artwork.
- `run_*.sh`: one-command runners for the principal controlled calculations.
- `requirements_*.txt`: method-specific Python dependencies.
- `ENVIRONMENT.txt`: tested software environment.
- `REPRODUCTION_COMMANDS.txt`: command-to-output map.
- `MANIFEST.tsv` and `SHA256SUMS.txt`: complete file inventory and integrity checks.

## Important interpretation limits

- The 3D DDA example verifies a complete geometry/source/open-domain/far-field workflow for a particle method; it is not a PML benchmark for FEM, FDTD, or FIT.
- The substrate calculation is an ED/MD layered-medium surrogate. The self-consistent ED comparison quantifies one omitted feedback contribution but is not an exact finite sphere-on-substrate full-wave solution.
- The physical 3 nm NPoM image-dimer surrogate is converged through `lmax = 16` for the reported optical observables. The 1 nm case remains a stress test and is explicitly reported as not converged to the same tolerance.
- The source-motivated 1.8 nm Au-trimer gap is a near-contact stress test. It remains more sensitive to multipole truncation than the 10 nm reference case.
- The archive intentionally excludes an internal slide-digitization audit that was labelled “DO NOT USE AS SUBMISSION DATA.”

## Persistent repository

This ZIP is deposit-ready. The corresponding author should upload the unchanged archive to Zenodo, OSF, Figshare, or an institutional repository, then insert the final DOI/URL in the manuscript Data Availability statement and submission metadata. No repository identifier is fabricated in this package.
