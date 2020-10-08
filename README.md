# Benchmark Quantum Chemistry Packages
Let's benchmark quantum chemistry packages! Who will be the winner?

## Benchmark results

**No.1**
- Molecule: C20 (charge = 0 and spin mult. = 1)<br>
- Task: Single-point energy calculation <br>
- Method: DFT B3LYP/6-31G(d)

|  **No. cores** | **Gaussian 09** | **Gaussian 16** | **ORCA 4.1.2** | **Turbomole 7.1** | **NWChem 7.0.0** | **Q-Chem 5.0** | **GAMESS-US 2020R1** | **PySCF** | **Psi4 1.3.2** | **Firefly 8.2.0** | **Dalton 2018** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  **1** | 191.4 | 535.1 | 573.0 | 205.0 | 1071.9 | 195.6 | 766.2 | 1758.9 | 726.2 | 1031.8 | 1502.0 |
|  **2** | 109.0 | 281.8 | 290.0 | 99.0 | 801.2 | 87.9 | 389.1 | 889.3 | 372.2 | 531.2 | 6215.0 |
|  **4** | 70.0 | 158.8 | 150.5 | 48.0 | 502.2 | 45.3 | 202.0 | 451.8 | 193.2 | 271.8 | 2142.0 |
|  **8** | 52.0 | 117.4 | 78.7 | 24.8 | 301.9 | 24.6 | 130.1 | 251.2 | 102.1 | 140.5 | 940.0 |
|  **16** | 43.0 | 68.6 | 45.5 | 14.2 | 179.2 | 16.7 | 90.1 | 135.5 | 60.2 | 79.3 | 456.0 |


## Note for computational details:
- Default DIIS
- Convergence criteria: energy diffeent cutoff is 1e-6
- GAMMES uses density difference
- Turbomol's RI-DFT is turned off
- Details of program and packages compilations: [click here](./compile/README.md)
- Specification of compute node: [click here](./misc/README.md)

## Next Plan?

1. MPI calculation
2. CCSD(T) calculation
3. Performance benchmarking on the robutness of geometry optimization engine
4. Frequency calculation

## Contact
All suggestions, comments, pull requestions, etc. are welcome. Please write us at r2compchem@gmail.com
