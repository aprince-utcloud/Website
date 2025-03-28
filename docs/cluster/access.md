## Accessing the PACC Cluster

### Web Access

Web Access at hpc.uthscsa.edu (LiCO)

The PACC Cluster can be accessed through the web interface at https://hpc.uthscsa.edu., which utilizes Lenovo Intelligent Computing Orchestration (LiCO). This interface provides a user-friendly way to manage and monitor your HPC jobs. This cluster can only be accessed while on our internal network. 

#### Steps to Access via Web Interface:
1. Open Your Browser: Navigate to An external link was removed to protect your privacy..
2. Login: Enter your HPC credentials to log in to the LiCO interface.
3. Dashboard: Once logged in, you will see the LiCO dashboard, where you can manage your jobs, monitor resource usage, and access various tools.
4. Submit Jobs: Use the job submission interface to submit your HPC jobs. You can specify job parameters, select resources, and monitor job progress.
5. Monitor Jobs: The dashboard provides real-time monitoring of your jobs, including resource usage, job status, and performance metrics.
6. Access Documentation: LiCO provides access to documentation and support resources to help you navigate and utilize the HPC cluster effectively.

### SSH Access at pacc.uthscsa.edu

For more advanced users, the PACC Cluster can also be accessed via SSH at pacc.uthscsa.edu This method allows for direct command-line interaction with the cluster.

#### Steps to Access via SSH:
1. Open Your Terminal: Launch your terminal application on your computer.
2. SSH Command: Use the following command to connect to the PACC Cluster:
```
ssh your_username@pacc.uthscsa.edu
```
3. Login: Enter your HPC credentials when prompted.
4. Command-Line Interface: Once logged in, you will have access to the command-line interface of the PACC Cluster. You can use various commands to manage your files, submit jobs, and monitor resource usage.
5. Submit Jobs: Use job submission commands (e.g., sbatch, srun) to submit your HPC jobs. Specify job parameters and resource requirements in your job scripts.
6. Monitor Jobs: Use commands like squeue, scontrol, and sacct to monitor job status, resource usage, and performance metrics.
7. Access Documentation: The command-line interface provides access to documentation and support resources to help you navigate and utilize the HPC cluster effectively.


### Internal Network Access and VPN Requirement

Access to the PACC Cluster is restricted to UT Health San Antonio's internal network. To ensure secure and reliable access, users must connect to the internal network using a Virtual Private Network (VPN).

#### Steps to Connect via VPN:
1. VPN Setup: Install the VPN client provided by UT Health San Antonio on your computer. Follow the installation instructions to configure the VPN client.
2. Connect to VPN: Launch the VPN client and connect to the UT Health San Antonio internal network using your credentials.
3. Access the Cluster: Once connected to the VPN, you can access the PACC Cluster via the web interface at https://hpc.uthscsa.edu. or via SSH at pacc.uthscsa.edu.

### Support and Contact Information
If you have any questions or need assistance with accessing the PACC Cluster, please contact the HPC administration team at hpc@uthscsa.edu. We are here to help you make the most of the PACC Cluster and ensure your research projects are successful