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
### Available Software on PACC
```
# Development Environments
- JupyterLab
- Jupyter Notebook
- Rstudio

# Programming Languages
- Julia
- Lua

# Annotation Tools
- CVAT

# Machine Learning Frameworks
- TensorFlow
- Caffe
- MXNet
- Neon

# Libraries
- cuDNN
- Nvidia CUDA
- Intel oneAPI

# Containers
- Singularity
- Charliecloud
- apptainer/main-gcc-13.2.0
- apptainer/1.1.9-gcc-13.2.0

# Bioinformatics Tools
- ants/2.5.1-gcc-13.2.0
- bam-readcount/1.0.1-gcc-13.2.0
- bcftools/1.19-gcc-13.2.0
- bedtools2/2.31.1-gcc-13.2.0
- bwa/0.7.17-gcc-13.2.0
- fastqc/0.12.1-gcc-13.2.0
- freesurfer/7.4.1-gcc-13.2.0
- gatk/4.5.0.0-gcc-13.2.0
- hisat2/2.2.1-gcc-13.2.0
- htslib/1.19.1-gcc-13.2.0
- kallisto/0.48.0-gcc-13.2.0
- mrtrix3/3.0.3
- nextflow/23.10.1-gcc-13.2.0
- picard/3.1.1-gcc-13.2.0
- pindel/0.2.5b8-gcc-13.2.0
- py-cutadapt/4.7-gcc-13.2.0
- rsem/1.3.3-gcc-13.2.0
- salmon/1.10.2-gcc-13.2.0
- samtools/1.19.2-gcc-13.2
- star/2.7.11a-gcc-13.2.0
- trimgalore/0.6.10-gcc-13
- varscan/2.4.2-gcc-13.2.0

# Compilers
- gcc/13.2.0

# Build Tools
- cmake/3.27.9-gcc-13.2.0

# Version Control
- git/2.45.1-gcc-13.2.0

# General Purpose Libraries
- boost/1.85.0-gcc-13.2.0
- zlib/1.3.1-gcc-11.4.1

# Visualization Libraries
- dcmtk/3.6.7-gcc-13.2.0
- qt/4.8.7-gcc-13.2.0
- qt/5.15.12-gcc-13.2.0
- javafx/20.0.1-gcc-13.2.0

# Package Managers
- miniconda3/24.3.0-gcc-13.2.0

# Programming Languages
- python/3.9.18-gcc-13.2.0
- python/3.10.13-gcc-13.2.0
- r/4.4.0-gcc-13.2.0

# Miscellaneous
- squashfuse/0.5.0-gcc-13
- perl-star-fusion/master-gcc-13.2.0
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