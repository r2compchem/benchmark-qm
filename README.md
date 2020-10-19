# Benchmark Quantum Chemistry Packages
Let's benchmark quantum chemistry packages! Who will be the winner?

## Packages for comparison:

Gaussian, ORCA, Turbomole, NWChem, Q-Chem, GAMESS-US, PySCF, Psi4, Firefly, Dalton

## Benchmark results

**No.1 : General test**
- Molecule: C20 (charge = 0 and spin mult. = 1)<br>
- Task: Single-point energy calculation <br>
- Method: DFT B3LYP/6-31G(d)

|  **No. cores** | **Gaussian 09** | **Gaussian 16** | **ORCA 4** | **Turbomole 7** | **NWChem 7** | **Q-Chem 5** | **GAMESS-US 2020** | **PySCF 1.7** | **Psi4 1.3** | **Firefly 8** | **Dalton 2018** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  **1** | 191.4 | 535.1 | 573.0 | 205.0 | 1071.9 | 195.6 | 766.2 | 1758.9 | 726.2 | 1031.8 | 1502.0 |
|  **2** | 109.0 | 281.8 | 290.0 | 99.0 | 801.2 | 87.9 | 389.1 | 889.3 | 372.2 | 531.2 | 6215.0 |
|  **4** | 70.0 | 158.8 | 150.5 | 48.0 | 502.2 | 45.3 | 202.0 | 451.8 | 193.2 | 271.8 | 2142.0 |
|  **8** | 52.0 | 117.4 | 78.7 | 24.8 | 301.9 | 24.6 | 130.1 | 251.2 | 102.1 | 140.5 | 940.0 |
|  **16** | 43.0 | 68.6 | 45.5 | 14.2 | 179.2 | 16.7 | 90.1 | 135.5 | 60.2 | 79.3 | 456.0 |

<p align="center">
   <img alt="benchmark_20.png" src="https://raw.githubusercontent.com/r2compchem/benchmark-qm/master/benchmark/bench_c20_cpu_b3lyp_631gd_def.png" align=middle width="900pt" />
<p/>

**No.2 : Gaussian 16 GPU**
- Molecule: C20 (charge = 0 and spin mult. = 1)<br>
- Task: Single-point energy calculation <br>
- Method: DFT B3LYP/6-31G(d)
- 4 x NVIDIA V100 SXM2 / Intel Xeon Gold 6132 CPU @ 2.60GHz

|  **No. actual used CPU cores** | **No GPU** | **1 GPU** | **2 GPUs** | **4 GPUs** |
| :---: | :---: | :---: | :---: | :---: |
|  **1** | 757.2 | 181.4 | 153.9 | 107.2 |
|  **2** | 406.5 | 157.5 | 134.2 | 97.5 |
|  **4** | 241.2 | 146.5 | 123.3 | 61.9 |
|  **8** | 164.6 | 88.4 | 70.8 | 56 |
|  **16** | 88.9 | 63.7 | 57.1 | 47.4 |

<p align="center">
   <img alt="benchmark_20.png" src="https://raw.githubusercontent.com/r2compchem/benchmark-qm/master/benchmark/bench_c20_g16_gpu_b3lyp_def.png" align=middle width="580pt" />
<p/>

## Note for computational details:
- Default DIIS
- Using default values of each package for convergence criteria, integral grids, etc.
- In ORCA, Psi4, and Turbomole, RI (or DF) approaximation is turned off
- Details of program and packages compilations: [click here](./compile/README.md)
- Specification of compute node: [click here](./misc/README.md)

## Disclaimers
We **do not** aim at showing the preference of one package over another, users should choose packages according to their:
1. Level of familiarity
2. Type of calculation
3. Hardwares availability

which are more important than a simple speed comparison.

## Next Plan?
1. MP2/cc-pVTZ calculation
2. CCSD(T)/cc-pVTZ calculation
3. Performance benchmarking on the robustness of geometry optimization engine
4. Frequency calculation

## Contact
All suggestions, comments, pull requests, etc are welcome. Please write us at r2compchem@gmail.com.
