This project had two main components: spectral line refitting and physical quantity derivation. These two files are the culmination of the entire projects that contains the framework code that was used in this project to produce metallicity values in NGC 4254, as well as the other 18 PHANGS-MUSE galaxies. This code is generalized to analyze other galaxies in the Nebular catalog; this same code has been restructed for analysis on other galaxies that also contain data from the SITELLE spectrograph at the CFHT. 

**INIT_LR_Pipeline.ipynb** This file contains the initial line refitting code for MUSE-PHANGS galaxies with SITELLE data. Faint emission lines, also known as auroral lines, are refitted to obtain flux values. The four auroral lines are [OII]7319,7330, [NII]5755, and [SIII]6312. Orgininally the background continuum was not subtracted in the Nebular catalog, so in this notebook I fit the auroral lines with a gaussian with a constant offset to account for the background continuum. The error in these measurements are calculated using monte carlo techniques. 

**INIT_PQ_Pipeline.ipynb** This file uses PyNeb to compute physical quantities using my refitted auroral lines and the nebular lines from the PHANGS Nebular catalog. These directly derived physical quantities include [NII], [SIII] and [OIII] temperatures, [SII] densities, and both elemental and ionic oyxgen abundances. 