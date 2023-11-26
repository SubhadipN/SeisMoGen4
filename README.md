# SEISmic MOtion GENarator (SeisMoGen)

## Description
Dynamic responses of a structure during any earthquake are approximately computed via nonlinear time-history analysis of any (idealized) 2D numerical model of the structure subjected to a unidirectional component of the ground motion. Therefore, the application of two orthogonal horizontal components of the ground motion on a 3D numerical model of the structure is necessary to get more realistic dynamic responses. In that case, the random simulation of bidirectional ground motions recorded along two orthogonal directions in the horizontal plane becomes useful to carry out the statistical study of dynamic responses of 3D structures via nonlinear time-history analysis. 

<a href="https://doi.org/10.1002/eqe.3537">Naskar and Das (2021)</a> introduced a new stochastic simulation methodology to generate bidirectional ground motions taking into account the frequency-dependent correlation structure of the underlying ground motion process. A Priestley process-based framework was adopted to address the nonstationarities in amplitudes and frequencies. The ***biseismogen.exe***, a Fortran-based computer program, is provided in this repository to generate $n\in[50,100]$ numbers of simulated bidirectional ground motion samples from the recorded data of a particular ground motion process following the methodology proposed by <a href="https://doi.org/10.1002/eqe.3537">Naskar and Das</a>.

## .exe file included in this repository

## How to use the .exe file

## Reference
<a href="https://doi.org/10.1002/eqe.3537">Naskar and Das (2021)</a>
