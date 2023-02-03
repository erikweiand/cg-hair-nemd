# cg-hair-nemd
*Nanoscale Friction of Biomimetic Hair Surfaces*  
E Weiand, JP Ewen, Y Roiter, PH Koenig, SH Page, F Rodriguez-Ropero, S Angioletti-Uberti and D Dini

**Maintainer / Corresponding author:**  
Erik Weiand  
Tribology Group, Imperial College London  
erik.weiand19@imperial.ac.uk  

This repository contains relevant files for producing coarse-grained molecular dynamics simulations (CG-MD) for contacts between two hair surfaces including squeeze-out and non-equilibrium molecular dynamics simulations (NEMD). Please consider citing our pre-print on bioRxiv<sup>[1]</sup> and Soft Matter hair surface paper<sup>[2]</sup> when using the material provided here.

**Example:** 25% hair damage (virgin hair) surface - squeeze-out and NEMD protocols available.

  Squeeze-out: Perform squeeze-out simulations in a water bath.
    1. Energy minimization (run.in.min)
    2. Brief NVT equilibration (run.in.nvt)
    3. Brief bulk pressure equilibration (run.in.npt)
    4. Surface compression at constant normal load of p=10MPa (run.in.comp)
    
  NEMD: Sliding between two hair surfaces at constant amount of water (from squeeze-out above) @ p=10MPa and v=0.1m/s.
    1. Energy minimization (run.in.min)
    2. Brief NVT equilibration (run.in.nvt)
    3. Compression at constant normal load (run.in.comp)
    4. NEMD (sliding) at v=0.1m/s (run.in.slide)
    
**Initial_Configs:** Initial LAMMPS topology files for wet hair contacts for squeeze-out simulations (01_SqueezeOut) and NEMD simulations at a normal contact pressure of 10MPa (02_NEMD) for all degrees of surface damage considered in our work. Initial configurations for NEMD simulations at other normal pressures can be obtained by running squeeze-out simulations. Dry contact NEMD simulations can be run by deleting all water molecules from the initial wet contacts.

**Moltemplate:** Scripts for setting up the water bath (squeeze-out) and water at contact (NEMD) for own simulations at arbitrary system dimensions and water content.

For making full use of this repository, the following tools should be accessible to the user:

    LAMMPS (https://www.lammps.org/)
    Moltemplate (https://www.moltemplate.org/)
    packmol (https://m3g.github.io/packmol/)
    A molecular visualization tool, such as VMD (https://www.ks.uiuc.edu/Research/vmd/)


## References
[1] E. Weiand, J. P. Ewen, Y. Roiter, P. H. Koenig, S. H. Page, F. Rodriguez-Ropero, S. Angioletti-Uberti, D. Dini, Nanoscale Friction of Model Hair Surfaces, bioRxiv (2022), https://doi.org/10.1101/2022.09.29.510078.

[2] E. Weiand, J. P. Ewen, P. H. Koenig, Y. Roiter, S. H. Page, S. Angioletti-Uberti, D. Dini, Coarse-grained molecular models of the surface of hair, Soft Matter 18 (2022), 1779-1792, https://doi.org/10.1039/D1SM01720A.
