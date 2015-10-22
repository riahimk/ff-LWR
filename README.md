# ff-LWR
This is a time-serial/parallel algorithm for the 3D neutrons calculation of a transient model in a nuclear reactor core. 
The neutrons calculation consists in numerically solving the time dependent diffusion approximation equation, which is a simplified transport equation.
The numerical resolution is done with finite elements method based on a tetrahedral meshing of the computational domain, representing the reactor core, and time discretization is achieved using a θ-scheme.
The transient model presents moving control rods during the time of the reaction. Therefore, cross-sections (piecewise constants) are taken into account by interpolations with respect to the velocity of the control rods. 
The parallelism across the time is achieved by an adequate use of the parareal in time algorithm to the handled problem. This parallel method is a predictor corrector scheme that iteratively combines the use of two kinds of
numerical propagators, one coarse and one fine

The program is auto-partitionner for time window just chose the number of processor that would process the parallel simulation and the program will adequate with mpi. 

