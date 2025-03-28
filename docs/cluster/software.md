# Software

## Overview

The PACC Cluster at UT Health San Antonio is equipped with a wide range of software tools and applications to support high-performance computing needs. This section provides information on the core software installed on the cluster and examples of how to check module availability and load applications.

## Core Software

The PACC Cluster includes the following core software:

- Operating Systems: Rocky Linux 9.3.
- Cluster Management: Lenovo LICO, Nagios/Ganglia.
- Resource Management: SLURM.
- Storage: NFS, Lustre, SMB, S3.
- Development Tools: GNU GCC, PGI, Intel Compilers, LAPACK, BLAS, MKL.
- Application Libraries: MVAPICH2, OpenMPI, Intel MPI, OpenMP, CUDA.
- Numerical Libraries: Performance and Debugging tools like PAPI, domain-specific libraries.
- ISV Applications: MathWorks, Ansys.
- Open Source Scientific Applications: Fortran, C, C++ and IDEs.

## Checking Module Availability

!!! note
    To check the availability of modules on the PACC Cluster, use the `module avail` command. This command lists all the available modules that you can load.


#### Example:
```
module avail
```

This command will display a list of available modules, including Conda, Python, R, and RStudio Server.

#### Loading Applications
To load an application, use the module load command followed by the name of the module. Here are examples of loading Conda, Python, R, and RStudio Server:

##### Loading Conda
```
module load conda
```
##### Loading Python
```
module load python
```
##### Loading R
```
module load R
```
##### Loading RStudio Server
```
module load rstudio-server
```
#### Example Job Script

Below is an example of a Slurm job script (job_script.sh) that loads Conda, Python, R, and RStudio Server modules and runs a Python script:
```
#!/bin/bash
#SBATCH --job-name=my_job          # Job name
#SBATCH --output=output.txt        # Output file
#SBATCH --error=error.txt          # Error file
#SBATCH --time=01:00:00            # Time limit (hh:mm:ss)
#SBATCH --partition=compute        # Partition name
#SBATCH --nodes=1                  # Number of nodes
#SBATCH --ntasks=1                 # Number of tasks
#SBATCH --cpus-per-task=4          # Number of CPUs per task
#SBATCH --mem=16G                  # Memory per node

# Load necessary modules
module load conda
module load python
module load R
module load rstudio-server

# Run your application
python my_script.py
```