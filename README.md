# Benchmark Quantum Chemistry Packages
Let's benchmark quantum chemistry packages! Who will be the winner?

**Benchmark results**

Molecule: C20 (charge = 0 and spin mult. = 1)<br>
Task: Single-point energy calculation <br>
Method: DFT B3LYP/6-31G(d)

|  **No. cores** | **Gaussian 09** | **Gaussian 16** | **ORCA 4.1.2** | **Turbomole 7.1** | **NWChem 7.0.0** | **Q-Chem 5.0** | **GAMESS-US 2020R1** | **PySCF** | **Psi4 1.3.2** | **Firefly 8.2.0** | **Dalton 2018** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  **1** | 191.4 | 535.1 | 573 | 205 | 1071.9 | 195.56 | 766.2 |  | 389.2 | 1031.8 | 1502 |
|  **2** | 109 | 281.8 | 290 | 99 | 801.2 | 87.86 | 389.1 | 889.2796617 | 200.2 | 531.2 | 6215 |
|  **4** | 70 | 158.8 | 150.5 | 48.01 | 502.2 | 45.33 | 202 | 451.7560856 | 105.2 | 271.8 | 2142 |
|  **8** | 52 | 117.4 | 78.7 | 24.82 | 301.9 | 24.55 | 130.1 | 251.1743373 | 57.5 | 140.5 | 940 |
|  **16** | 43 | 68.6 | 45.5 | 14.19 | 179.2 | 16.65 | 90.1 | 135.4870663 | 36.6 | 79.3 | 456 |
|  **16*2** | 48 |  |  |  |  |  |  | 171.6033206 | 37.9 |  |  |

Compilation details: [click here](./compile/README.md)

## Note for computational details:
- Default DIIS
- Convergence criteria: energy diffeent cutoff is 1e-6
- GAMMES uses density difference
- Turbomol's RI-DFT is turned off

<br>

**specification**


|   |   |
| --- | --- |
|  Architecture | x86_64 |
|  CPU op-mode(s) | 32-bit, 64-bit |
|  CPU(s) | 32 |
|  Thread(s) per core | 2 |
|  core(s) per socket | 16 |
|  Socket(s) | 1 |
|  NUMA node(s) | 1 |
|  Vendor ID | authenticAMD |
|  Model name | AMD Ryzen Threadripper 1950X 16-Core Processor |
|  CPU MHz | 3600 |
|  No. of processors | 16 |
|  Total Memory/proc | 2 GB |

## Contact
All suggestions, comments, pull requestions, etc. are welcome. Please write us at r2compchem@gmail.com
