These are the results for EXX calculations for H, H2, F, F2, HF

We can compare the energies with https://arxiv.org/pdf/2208.14726.pdf

In VASP, we use alavi-spencer truncation with
12A box length and ENCUT=800 for all calculations.\
Units in eV

|mol | enc800    | enc600|
|--- | ---       | ---   |
|HF  | -17.68817 | -17.67155 |
|F2  | -17.06572 | -17.04343 |
|F   |  -9.46555 |  -9.45387|
|H2  | -11.72874 | -11.72483 |
|H   |  -4.04161 | -4.04122 |


box with 10A

|mol | enc800    | enc600|
|--- | ---       | ---   |
|HF  | -17.69060 | -17.67380 |
|F2  | -17.06650 | -17.04405 |
|F   |  -9.46578 |  -9.45396 |
|H2  | -11.72886 | -11.72492 |
|H   |  -4.04190 | -4.041492 |

Atomization energies in kcal/mol (23.061):

| mol | own 12A (800/600) | own 10A (800/600)| paper-vasp |  tmole |
| --- | ---    | ---    | ---        |  ---   |
| H2  |  84.07 /  84.00  | 84.06 / 83.97| 83.92     |  84.07 |
| F2  | -43.02 / -42.99  | -43.01 / 42.98|-42.60     | -42.61 |
| HF  |  96.39 /  96.31  | 96.46 / 96.36| 96.29     |  96.42 |
