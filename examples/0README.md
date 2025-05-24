The GT_* files contain the results from a 6.3 μs folding simulation of the CLN025 peptide using the AMBER-99SB-ILDN force field. 

The graphs are in the PDF files (as produced by R). 

The file 'GT_Screenshot.png' is the log produced on the interactive shell.

The file 'Comparison.png' illustrates the form of the results for simulations of different peptides/proteins (and with different simulations lengths). The Good-Turing graphs offer quantitative estimates of the probability of observing significantly different structures if we continue the current simulation. In this example, the red curve is from a simulation in the folded state of a stable protein (ROP), and G-T shows that nothing dramatic is expected to happen if we continue the simulation (the probability falls to zero at ~0.7Å). The other graphs are from _folding_ simulations which explains the higher RMSDs. 6NM2 appears to be the best sampled simulation (probability falls to approximately zero at ~1.5Å), followed by CLN025, and finally FipWW (for which we can reasonably expect to observe very different structures if we were to continue the simulation).

