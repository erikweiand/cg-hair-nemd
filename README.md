# cg-hair-nemd
Coarse-grained NEMD of hair friction phenomena.

Work in progress - 22/09/28.

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
