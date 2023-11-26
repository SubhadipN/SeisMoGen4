![Logo](https://lh3.googleusercontent.com/drive-viewer/AK7aPaBeEVShCCPjBw7h2LsnRh3r0nz-ndunaItNz0O5jR8830_Cv7sfDqeMmBfl_29jRjBVlIxgiPwuTdCpJ2cKF9j_tTTf=s2560)

# SEISmic MOtion GENarator (SeisMoGen)

## Description
Dynamic responses of a structure during any earthquake are approximately computed via nonlinear time-history analysis of any (idealized) 2D numerical model of the structure subjected to a unidirectional component of the ground motion. Therefore, the application of two orthogonal horizontal components of the ground motion on a 3D numerical model of the structure is necessary to get more realistic dynamic responses. In that case, the random simulation of bidirectional ground motions recorded along two orthogonal directions in the horizontal plane becomes useful to carry out the statistical study of dynamic responses of 3D structures via nonlinear time-history analysis. SeisMoGen4 can be used to simulate $n(\leq 100)$ number of pairs of random bidirectional samples from acceleration values recorded along two orthogonal horizontal directions during a seismic event. The fully nonstationary (amplitude and frequency) artificial samples are simulated using the Priestley process-based methodology (refer to Section 2 of this <a href="https://doi.org/10.1002/eqe.3537">article</a>) and they are oriented along the corresponding recording directions.

## Instruction to use SeisMoGen4
  1. Download SeisMoGen4.rar from [here](https://drive.google.com/file/d/1Ow1-BrQRcV0Y9EC4IGDMaHvTG9q1oOWn/view?usp=sharing).
  2. Extract SeisMoGen4.rar within a suitable folder.
  3. Keep the recorded bidirectional ground motion file in the same folder where SeisMoGen4.exe resides.
     1. The ground motion file must be in a 3-column format with the following values.
        * 1st column: time instants
        * 2nd column: acceleration along recording direction 1
        * 3rd column: acceleration along recording direction 2
     2. The incremental time-step of the 1st column must be 0.02 seconds.
  4. Run SeisMoGen4.exe.

## Reference
<a href="https://doi.org/10.1002/eqe.3537">Naskar and Das (2021)</a> "Bi-directional ground motions: Stochastic simulation and frequency-dependent modal combination rule", <i>Earthquake Engineering & Structural Dynamics</i>, Vol. 50(14), pp. 3872-3893.
