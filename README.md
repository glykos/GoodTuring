# GoodTuring
A memory-efficient application of Good-Turing statistics to quantify the uncertainty of molecular dynamics simulations.

## Description
This is a variation of the Good-Turing application to molecular dynamics trejectories reported in : Koukos, P.I. & Glykos*, N.M. (2014), "On the application of Good-Turing statistics to quantify convergence of biomolecular simulations", J. Chem. Inf. Model., 54, 209-217. http://dx.doi.org/10.1021/ci4005817

It attempts to bypass the significant memory limitations of the original algorithm by avoiding the calculation of the whole RMSD distance matrix. The principal idea is that instead of calculating and storing in memory the whole matrix (and then preparing a dendrogram), we calculate and keep for each row of the matrix only the highest RMSD observed, and we then assume that this largest RMSD would correspond -if we could make a dendrogram- to single-membered cluster (and can thus be used to calculate the Good-Turing probability). 

The initial part of script calculates successive superdiagonals of the matrix which then uses to estimate the sampling step needed to obtain 'independent' structures. The treatment is essentialy identical with the originally reported procedure.

## Requirements
To use this program, you'll need a molecular dynamics trajectory (only DCD+PSF supported), the latest version of the program 'carma' from https://utopia.duth.gr/glykos/progs/ and the R package for statistical computing with the dpseg & minpack.lm libraries installed.
