# Storage

Overview
The PACC Cluster at UT Health San Antonio provides robust and scalable storage solutions to support high-performance computing needs. Our storage infrastructure is designed to handle large-scale data sets, long-term data retention, and active workloads efficiently.

### Storage Options
#### High-Performance Storage
Our high-performance storage is optimized for active workloads and large data sets. The DDN cluster offers high-performance storage with a minimum requested storage amount of 1 TB, available in 1 TB increments.

#### Archival Storage
Archival storage is designed for long-term data retention and is available at competitive rates.  available in 1 TB increments.

UT Health San Antonio Faculty and Staff: Faculty and staff can request PACC archival storage for research data without a PACC allocation.

#### Access Protocols
Storage can be configured for access through either SMB or NFS protocols. IMS provides user access management through SMB protocols, while NFS access management is handled by the department.
For detailed pricing information, please refer to the [pricing table](#pricing) pricing table listed below.

### Storage Management
Our storage management solutions ensure efficient handling of data usage and quotas:

* Data Redundancy and High Availability: Mechanisms for ensuring high availability, data redundancy, and fault tolerance.
* Data Management Tools: Solutions for moving and migrating data between different storage types to balance cost and performance.
Storage Protocols and Snapshots
We support various storage protocols and snapshots to meet diverse needs:

* Supported Protocols: NFS, SMB, S3, and POSIX.
* Snapshots: Snapshots are supported to ensure data integrity and recovery.


### Data Movement with Globus
Globus is a powerful data transfer and management tool that facilitates efficient and secure data movement across different storage systems. It is widely used by researchers, research computing managers, IT groups, and developers to manage large-scale data transfers.

#### Key Features of Globus:
* Efficient Data Movement: Globus enables fast and reliable data transfers, even for large files and datasets. It uses automated client-driven chunking to accelerate data movement and integrity checking.
* Data Sharing: Users can easily share data with collaborators, regardless of where the data is stored. Globus supports data sharing across supercomputers, lab clusters, tape archives, public clouds, and personal devices.
* User-Friendly Interface: Globus provides a single interface for managing data transfers, making it easy to move, share, and discover data from anywhere using a web browser.
* Integration with PACC Cluster: Globus is integrated with the PACC Cluster, allowing users to access their data on Isilon and other shares without needing to mount them directly to the cluster.

#### Steps to Use Globus for Data Movement:
1. Access Globus: Navigate to the Globus web interface https://app.globus.org and log in using your credentials.
2. Select Endpoints: Choose the source and destination endpoints for your data transfer. Endpoints can be any storage system supported by Globus.
3. Initiate Transfer: Specify the files or directories you want to transfer and initiate the transfer process. Globus will handle the data movement efficiently and securely.
4. Monitor Transfer: Use the Globus interface to monitor the progress of your data transfer. You can view transfer status, performance metrics, and any errors that may occur.

#### Globus Help
For detailed instructions and troubleshooting tips on using Globus, please refer to our Knowledge Base (KB) article: [UT Health SA Globus KB](https://uthscsa.teamdynamix.com/TDClient/2009/Portal/KB/ArticleDet?ID=92169)

## Quotas

### Condo Owners Storage & Backup Schedule
| Storage Type     | PATH     | Quota                | Backup | Purge              |
| ---------------- | -------- | -------------------- | ------ | ------------------ |
| Home Directories | /home    | 100GB                | Daily  | None               |
| Project          | /project | 1TB                  | Daily  | None               |
| Scratch          | /scratch | as available on node | None   | Older than 90 days |


### Community Members Storage & Backup Schedule 
| Storage Type     | PATH     | Quota                | Backup | Purge              |
| ---------------- | -------- | -------------------- | ------ | ------------------ |
| Home Directories | /home    | 100GB                | Daily  | None               |
| Project          | /project | 300GB                | Daily  | None               |
| Scratch          | /scratch | as available on node | None   | Older than 90 days |

## Pricing 

| Storage type                       | Minimum increment | Total Cost per TB | Protocol |
| ---------------------------------- | ----------------- | ----------------- | -------- |
| SSD (PACC - Condo Partner)         | 1 TB              | $217.00           | NFS      |
| SSD (PACC - Subscription & Hotel)  | 1 TB              | $313.00           | NFS      |
| HDD (PACC - Condo Partner)         | 1 TB              | $27.00            | NFS      |
| HDD (PACC - Subscription & Hotel)  | 1 TB              | $40.00            | NFS      |
| HDD (Non-PACC  – Researchers only) | 1 TB              | $55.00            | SMB/NFS  |