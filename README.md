# XTRACT_Macaque_MultiTemplate
XTRACT protocols for the Rhesus Macaque in 5 template spaces (F99, D99, NMTv2.0, INIA, Yerkes19).

### Overview ###
XTRACT tractography protocols for the Macaque were originally developed using the F99 template space.
However, there are various other templates commonly used. 

Our F99-space protocols were transformed to 4 other macaque template spaces using the RheMAP pipeline, which is based on ANTs non-linear registration. 
These templates were based on both in-vivo and ex-vivo anatomical (T1w) MRI data and included: D99, INIA19, NMTv2.0, Yerkes19 (YRK).

This repository includes a directory per template space, with each containing:
1. A structural MR image in that space to be used as a reference.
2. XTRACT tractography protocols (ie seed, target, exclusion ROIs) for 42 White Matter (WM) fibres, covering major association, commissural, projection and limbic fibres.

### Generalisation Method ###

- ANTs non-linear warp fields (obtained from Rhe-MAP) were converted to FSL format (to be used with XTRACT).
  
- Certain protocols in the new template spaces were manually refined where registration caused imperfections (for instance in cases of CBP, CST and AC). Specifcially, modifications to the exclusion, seed and target ROIs were performed (where necessary) to achieve bilateral symmetry, as well as avoid ROI overlap and eliminate mapping outside the brain when transformed to the other template spaces.
  
- Subject-wise non-linear transformations to each template space were obtained using FSL's FNIRT, based on subject FA maps. 
