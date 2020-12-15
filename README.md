# Auto-align
Python implementation of code to align protein by weighting the most stable residues higher than more flexible ones.

## Requirements
Requires python environment with numpy and MDanalysis. It is easy to make you own using conda, but you can also use this one:

 conda activate /home/agp2004/anaconda3/envs/tica_env
 
 ## Theory
Uses a distance matrix for each frame of the simulation to calculate the mean fluctuation of each alpha carbon. Alpha carbons of stable residues will reflect the fluctations of the other residues. Alpha carbons of flexible residues will reflect the fluctations of the other residues AND their own fluctuations. The alignment is then weighted by the inverse of the mean fluctuation of each alpha carbon. Feel free to play with this weighting scheme.
 
 ## Usage
 Commmand line:

align.py $input.psf $input.dcd $aligned.dcd
