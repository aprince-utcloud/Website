# Job Submission

### Overview
Submitting jobs to the PACC Cluster is a straightforward process that allows you to leverage the high-performance computing resources for your research projects. This section provides detailed instructions on how to submit jobs using both the web interface and SSH.

### Web Interface at hpc.uthscsa.edu (LiCO)
The PACC Cluster can be accessed through the web interface at An external link was removed to protect your privacy., which utilizes Lenovo Intelligent Computing Orchestration (LiCO). This interface provides a user-friendly way to manage and monitor your HPC jobs.

#### Steps to Submit Jobs via Web Interface:
1. Open Your Browser: Navigate to An external link was removed to protect your privacy..
2. Login: Enter your HPC credentials to log in to the LiCO interface.
3. Dashboard: Once logged in, you will see the LiCO dashboard, where you can manage your jobs, monitor resource usage, and access various tools.
4. Submit Jobs: Use the job submission interface to submit your HPC jobs. You can specify job parameters, select resources, and monitor job progress.
5. Monitor Jobs: The dashboard provides real-time monitoring of your jobs, including resource usage, job status, and performance metrics.
6. Access Documentation: LiCO provides access to documentation and support resources to help you navigate and utilize the HPC cluster effectively.
SSH Access at pacc.uthscsa.edu
For more advanced users, the PACC Cluster can also be accessed via SSH at An external link was removed to protect your privacy.. This method allows for direct command-line interaction with the cluster.

### Steps to Submit Jobs via SSH:
1. Open Your Terminal: Launch your terminal application on your computer.
2. SSH Command: Use the following command to connect to the PACC Cluster:
ssh your_username@pacc.uthscsa.edu
3. Login: Enter your HPC credentials when prompted.
4. Command-Line Interface: Once logged in, you will have access to the command-line interface of the PACC Cluster. You can use various commands to manage your files, submit jobs, and monitor resource usage.
5. Submit Jobs: Use job submission commands (e.g., sbatch, srun) to submit your HPC jobs. Specify job parameters and resource requirements in your job scripts.
6. Monitor Jobs: Use commands like squeue, scontrol, and sacct to monitor job status, resource usage, and performance metrics.
7. Access Documentation: The command-line interface provides access to documentation and support resources to help you navigate and utilize the HPC cluster effectively.


### Example of Submitting a Slurm Job

#### Slurm Job Script
Below is an example of a Slurm job script (job_script.sh) with definitions for each part:
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
module load python/3.8

# Run your application
python my_script.py
```

#### Definitions
```
* #!/bin/bash: Specifies the shell to use for the script.
* #SBATCH --job-name=my_job: Sets the name of the job.
* #SBATCH --output=output.txt: Specifies the file to which standard output will be written.
* #SBATCH --error=error.txt: Specifies the file to which standard error will be written.
* #SBATCH --time=01:00:00: Sets the time limit for the job (1 hour in this example).
* #SBATCH --partition=compute: Specifies the partition to use for the job.
* #SBATCH --nodes=1: Sets the number of nodes to use.
* #SBATCH --ntasks=1: Sets the number of tasks to run.
* #SBATCH --cpus-per-task=4: Sets the number of CPUs per task.
* #SBATCH --mem=16G: Sets the memory per node (16 GB in this example).
* module load python/3.8: Loads the necessary module (Python 3.8 in this example).
* python my_script.py: Runs the application (a Python script in this example).
```
#### Submitting the Job
To submit the job, use the following command:
```
sbatch job_script.sh
```