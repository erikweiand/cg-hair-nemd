# cg-hair-nemd
Coarse-grained NEMD of hair friction phenomena.

Please consider citing our pre-print on bioRxiv<sup>[1]</sup> and Soft Matter hair surface paper<sup>[2]</sup> when using the material provided here.

Work in progress - 11/01/28.

Example: 25% hair damage (virgin hair) surface - squeeze-out and NEMD protocols available.

  Squeeze-out: Perform squeeze-out simulations in a water bath.
    1. Energy minimization (run.in.min)
    2. Brief NVT equilibration (run.in.nvt)
    3. Brief bulk pressure equilibration (run.in.npt)
    4. Surface compression at constant normal load of p=10MPa (run.in.comp)
    
  NEMD: Sliding between two hair surfaces at constant amount of water (from squeeze-out above) @ p_N=10MPa and v=0.1m/s.
    1. Energy minimization (run.in.min)
    2. Brief NVT equilibration (run.in.nvt)
    3. Compression at constant normal load (run.in.comp)
    4. NEMD (sliding) at v=0.1m/s (run.in.slide)

## References
[1] E. Weiand, J. P. Ewen, Y. Roiter, P. H. Koenig, S. H. Page, F. Rodriguez-Ropero, S. Angioletti-Uberti, D. Dini, Nanoscale Friction of Model Hair Surfaces, bioRxiv (2022), https://doi.org/10.1101/2022.09.29.510078.

[2] E. Weiand, J. P. Ewen, P. H. Koenig, Y. Roiter, S. H. Page, S. Angioletti-Uberti, D. Dini, Coarse-grained molecular models of the surface of hair, Soft Matter 18 (2022), 1779-1792, https://doi.org/10.1039/D1SM01720A.
