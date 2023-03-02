Results for using different Gaussian basis sets using nwchem.\
CN: cardinal number of the basis set\
NB: number of basis functions\
HF energy and MP2/CCSD correlation energy\
Correlation energies are currently using frozen core approx.\


aug-cc-pvXz

| CN | NB| HF | MP2 | CCSD |
|--- | ---|---| ---| ---|
| 2 |  32 | -100.0335 | -0.2222 | -0.2259 |
| 3 |  69 | -100.0611 | -0.2797 | -0.2809 |
| 4 | 126 | -100.0686 | -0.3011 | -0.3005 |
| 5 | 207 | -100.0707 | -0.3099 | -0.3074 |
|[45] | - |     -     | -0.3191 | -0.3146 |

aug-cc-pcvXz

this is possible because we can use CV for F and normal for H


| CN | NB |HF | MP2 | CCSD |
|--- | ---|---| ---| ---|
| 2 |  36 | -100.0337 | -0.2260 | -0.2293 |
| 3 |  82 | -100.0613 | -0.2847 | -0.2854 |
| 4 | 155 | -100.0687 | -0.3037 | -0.3025 |
| 5 | 261 | -100.0707 | -0.3111 | -0.3084 |
|[45]| -  |    -      | -0.3189 | -0.3146 |

Results from exciting.

The table contains: 
* box - the unit cell parameter (a0),
* rgkmax - dimensionless LAPW cutoff R\_MT * |G+k|\_max (muffin-tin radius times longest wavevector),
* NB - number of basis functions,
* total energies.
R_H=0.7 a_0, R_F=1.0 a_0. 

| box | rgkmax | NB | HF | MP2 | CCSD |
|--- | ---| ---|---| ---| ---|
| 15  | 5.4  | 26237  | -100.07028 | | |
| 15  | 6.3  | 41847  | -100.07080 | | |
| 15  | 7.0  | 57143  | -100.07080 | | |
| 20  | 7.0  | 135135 | -100.07079 | | |

Reaction energy E(HF)-0.5\*E(H2)-0.5\*E(F2) in eV. Conversion factor 27.211 eV/Ha.

| box | rgkmax | Reaction (HF) | 
|--- | ---| ---|
| 15  | 5.4  |  -3.181 |
| 15  | 6.3  |  -3.188 |
| 15  | 7.0  |  -3.187 |
| 20  | 7.0  |  -3.192 |
