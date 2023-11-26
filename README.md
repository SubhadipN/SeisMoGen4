![Logo](https://lh3.googleusercontent.com/drive-viewer/AK7aPaBeEVShCCPjBw7h2LsnRh3r0nz-ndunaItNz0O5jR8830_Cv7sfDqeMmBfl_29jRjBVlIxgiPwuTdCpJ2cKF9j_tTTf=s2560)

# SEISmic MOtion GENarator (SeisMoGen)

## Description
Dynamic responses of a structure during any earthquake are approximately computed via nonlinear time-history analysis of any (idealized) 2D numerical model of the structure subjected to a unidirectional component of the ground motion. Therefore, the application of two orthogonal horizontal components of the ground motion on a 3D numerical model of the structure is necessary to get more realistic dynamic responses. In that case, the random simulation of bidirectional ground motions recorded along two orthogonal directions in the horizontal plane becomes useful to carry out the statistical study of dynamic responses of 3D structures via nonlinear time-history analysis. SeisMoGen4 can be used to simulate $n(\leq 100)$ number of pairs of random bidirectional samples from acceleration values recorded along two orthogonal horizontal directions during a seismic event. The fully nonstationary (amplitude and frequency) artificial samples are simulated using the Priestley process-based methodology (refer to Section 2 of this <a href="https://doi.org/10.1002/eqe.3537">article</a>) and they are oriented along the corresponding recording directions.

## Instruction to use SeisMoGen4
----
1. Download SeisMoGen4.rar from [here](https://drive.google.com/file/d/1Ow1-BrQRcV0Y9EC4IGDMaHvTG9q1oOWn/view?usp=sharing).
2. Extract SeisMoGen4.rar within a suitable folder.
3. Keep the recorded bidirectional ground motion file in the same folder where SeisMoGen4.exe resides. Two sample files (*target_moiton_01.dat* and *target_moiton_02.dat*) with acceleration values recorded along two directions are included within SeisMoGen4. The ground motion file must be in a 3-column format with the following values.
   >* 1st column: time instants
   >* 2nd column: acceleration along recording direction 1
   >* 3rd column: acceleration along recording direction 2
4. Run SeisMoGen4.exe.
   <p align="center"> <img align="center" src="SeisMoGen4_demo.png.png" alt="drawing" width="500"/> </p>
   <p align="center"> Screenshot of the software after Step 4 </p>
6. Enter the name of the input file including some necessary information to simulate the artificial motions. A sample input file (*SeisMoGen4_input.dat*) is included within SeisMoGen4. However, other input files with different names and/or different extensions can also be used, provided they include the following row-wise details (similar to *SeisMoGen4_input.dat*).
   >* 1st column: filename of the target recorded bidirectional ground motion (e.g., *target_moiton_01.dat* and *target_moiton_02.dat*), which will be used to generate simulated motions.
   >* 2nd column: name of the folder (e.g., *simulated_folder_01* or *simulated_folder_02*) where the simulated files will be stored.
   >* 3rd column: required number (less than 100) of pairs of simulated bidirectional ground motions (e.g., 50).
----

> [!IMPORTANT]
> 1. The details provided in the input file will generate the required number of pairs of bidirectional motions corresponding to multiple target-recorded motions in a single run and store them in separate user-defined folders.
> 2. The simulated motion files contain data in the 3-column format similar to the target recorded bidirectional ground motion file (e.g., *target_moiton_01.dat* and *target_moiton_02.dat*).
> 3. The simulated motions are baseline-corrected and high-pass filtered with a cutoff frequency of 0.1Hz using Butterworth filter (order = 1).

> [!CAUTION]
> For successful execution of SeisMoGen4.exe, following conditions must be satisfied.
> * The incremental time-step (i.e., the difference between any two consecutive rows of the 1st column) of the target recorded files (e.g., *target_moiton_01.dat* and *target_moiton_02.dat*) must be 0.02 seconds.
> * The required number of pairs of simulated motions (i.e., the value prescribed in the 3rd column of the input file similar to *SeisMoGen4_input.dat*) must be less than 100.
> * The number of rows available in the user-defined input file must not exceed 1000. It means the program can generate artificial motions corresponding to not more than 1000 target bidirectional motions in a single run. If someone needs to simulate random motions corresponding to more numbers of target motions, the program must be executed more than once.

## Reference
<a href="https://doi.org/10.1002/eqe.3537">Naskar and Das (2021)</a> "Bi-directional ground motions: Stochastic simulation and frequency-dependent modal combination rule", <i>Earthquake Engineering & Structural Dynamics</i>, Vol. 50(14), pp. 3872-3893.
