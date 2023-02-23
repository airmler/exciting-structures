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

Atomization energies in kcal/mol (23.061):

| mol | own-Vasp (800/600) | paper-vasp |  tmole |
| --- | ---      | ---        |  ---   |
| H2  |  84.07 /  84.00  |  83.92     |  84.07 |
| F2  | -43.02 / -42.99  | -42.60     | -42.61 |
| HF  |  96.39 /  96.31  |  96.29     |  96.42 |
