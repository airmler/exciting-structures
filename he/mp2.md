Summary on MP2 for He.

Attached files

Inputs: 
* input.xml - the main input file.
* He.xml - species file, defines the basis within the muffin tin.

Postprocessing:
* he-nvirt.pdf - the MP2 correlation energy vs. the number of virtuals in three calculations using different muffin-tin radii, rmt=1.5, 2.0 and 3.0.
* he-extrapolation.pdf - an attempt to extrapolate the correlation energy to the CBS limit in the rmt=1.5 calculation.

Computational details
The APW cutoff is rgkmax=6 and it is the same in all three calculations. This dimensionless parameter is defined as the smallest MT radius times the longest |G+k|. If the the MT radius (rmt) is changed, the number of APWs gets adjusted too. The other component of the basis is local orbitals that are non-zero strictly within a MT. In all calculations, I have set up 18 s-, 5 p-, 4 d-, 4 f-, 2 g-, 2 h- and 2 i-shells of local orbitals without too much thinking and without trying to achieve convergence w.r.t. them. 

Actually, there is a small inconsistency in the number of LOs between rmt=3.0 and rmt=1.5,2.0. Apparently, I have added too many LOs in the rmt=1.5,2.0 calculations. It is easy to fix the inconsistency if necessary.

The calculations consist of two steps: a Hartree-Fock run using the mixed-basis formalism (not ACE for now), an MP2 step using the mixed-basis approach implemented by a quick-and-dirty modification of the GW code (taskname="g0w0").

Results
The calculated MP2 correlation energies and the number of the basis functions in the calculations are given in the table below.

| rmt [a0] | APWs | LOs | E_c [mHa] |
|--- | ---| ---| ---|
| 1.5  | 1045  |  154 | -36.6 |
| 2.0  | 461  | 154 | -36.3 |
| 3.0  | 147  | 147 | -34.0 |

A small sidenote. There is a small inconsistency in the number of LOs between rmt=3.0 and rmt=1.5,2.0. Apparently, I have added too many LOs in the rmt=1.5,2.0 calculations. It is easy to fix the inconsistency if necessary.

The reference value for the comparison is -37.4 mHa from J R Flores and D Kolb, J. Phys. B: At. Mol. Opt. Phys. 32, 779 (1999), https://iopscience.iop.org/article/10.1088/0953-4075/32/3/019/meta. The agreement probably could be improved, by extending the basis in each calculation. Adding more basis functions is straightforward.

Fig. he-nvirt.pdf shows how the correlation energy depends on the number of virtuals. The rmt=1.5, 2.0 and 3.0 calculations have spot-on agreement until the number of augmented plane-waves is exceeded for run with a smaller basis. When this happens, the virtual orbitals are described almost solely by LOs. 

Fig. he-extrapolation.pdf shows an attempt to extrapolate the correlation energy to the CBS limit. Here is my procedure:
* Step 1. Choose an estimate for the CBS limit, E(CBS).
* Step 2. Perform a linear regression for 1/(E(Nvirt)-E(CBS)). In this fit, 1 <= Nvirt <= Napw.
* Step 3. Repeat steps 1 and 2 to find such E(CBS) that minimises R^2.

This procedure applied to the rmt=1.5 data yields E(CBS)=-36.9 mHa, and the result agrees well with the direct calculation and the benchmark reference. However, the step-like dependence looks concerning. The question is how large part of the unoccupied spectrum do we need to take to make the extrapolation reliable?

Failed calculations

An all-band ACE calculation with a Coulomb cutoff (V=4\*pi/G^2\*(1-cos(G\*R)) falls apart, because the exchange matrix is not negative-defined anymore. Calculations with 20-40% of the spectrum work, but it has be inverstigated where they brings us. Moreover, there is a fundamental question: is it meaningful to apply the Coulomb cutoff for a delocalised product of two virtual orbitals? This is irrelevant in the MP2 case, but it is in the case of coupled clusters.

Runs with a minimum set of LOs
The large number of LOs is essential to get the cusp right. What happens if we leave just 2 LOs in the s-channel?

| rmt [a0] | APWs | LOs | E_c [mHa] |
|--- | ---| ---| ---|
| 1.5  | 1045  |  2 | -18.0 |
| 2.0  | 461  | 2 | -11.7 |
| 3.0  | 147  | 2 | -4.2 |

The poorly resolved region shrinks with reducing rmt, and the correlation energy improves, but it is awful even for the smallest considered rmt. 
