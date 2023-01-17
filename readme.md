# MD Simulation of HsNHA2 Bound to Phloretin

## System Setup

All simulations were run using HsNHA2 cryo-em structure - PDB entry 
7B4L at 3.1 Angstrom resolution.

### pH Calculations

To model the pH gradient across the membrane titratable residues' 
protonation states were determine in pH 5.0 for residues facing the 
extra-cellualr matrix and pH 7.0 for residues facing the cytoplasm.

pKa values were determined using Propka Version 3.4.0 via the PDB2PQR
webserver with the CHARMM force field and naming scheme

| Residue | pKa  | Buried | In/Out    | Protonation State   | 
|---------|------|--------|-----------|---------------------|
| Asp 85  | 5.0  | 15%    | In (7.0)  | Charged             |
| Asp 164 | 3.97 | 0%     | Out (5.0) | Charged             |
| Asp 278 | 9.03 | 100%   | Buried    | **Neutral**         |
| Asp 279 | 5.25 | 100%   | Buried    | **Neutral/Charged** |
| Asp 331 | 3.75 | 0%     | In (7.0)  | Charged             |
| Asp 394 | 4.96 | 43%    | In (7.0)  | Charged             |
| Asp 473 | 4.61 | 26%    | Out (5.0) | Charged             |
| Asp 485 | 3.87 | 0%     | Out (5.0) | Charged             |
| Asp 489 | 5.84 | 55%    | Out (5.0) | **Neutral (1)**     |
| Glu 108 | 4.77 | 22%    | Out (5.0) | Charged             |
| Glu 215 | 5.55 | 100%   | Buried    | **Charged (2)**     |
| Glu 264 | 5.59 | 0%     | In (7.0)  | Charged             |
| Glu 309 | 7.29 | 59%    | Buried    | **Charged (3)**     |
| Glu 381 | 4.07 | 23%    | In (7.0)  | Charged             |
| Glu 384 | 3.94 | 0%     | In (7.0)  | Charged             |
| Glu 386 | 6.00 | 53%    | In (7.0)  | Charged             |
| Glu 407 | 6.00 | 83%    | Out (5.0) | **Cahrged (4)**     |
| Glu 416 | 4.43 | 0%     | Out (5.0) | Charged             |
| Glu 449 | 4.32 | 24%    | In (7.0)  | Charged             |
| Glu 480 | 4.73 | 0%     | Out (5.0) | Charged             |
| Glu 484 | 4.47 | 0%     | Out (5.0) | Charged             |
| Glu 521 | 3.61 | 0%     | In (7.0)  | Charged             |
| His 81  | 7.12 | 0%     | In (7.0)  | HSP                 |
| His 170 | 6.03 | 26%    | Out (5.0) | HSP                 |
| His 224 | 6.02 | 0%     | Out (5.0) | HSP                 |
| His 356 | 6.11 | 2%     | Out (5.0) | HSP                 |
| His 478 | 6.27 | 0%     | Out (5.0) | HSP                 |

(1) pKa higher than pH and also spatially close to Asp 485.

(2) Buried and pKa higher than pH **but** spatially close to Lys 460.

(3) Buried but spatially close to Arg 305.

(4) pKa heigher that pH and buried, *but* spatially close to Arg 157 ; His 170 ; Arg 177 .

**All Lys and Arg residues are charged.**

### Missing Atoms
Asp 473: Missing side chain