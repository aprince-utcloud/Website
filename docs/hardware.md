# This will show hardware details

## PACC Cluster Hardware Overview


| Cluster Configuration Type | Lenovo Intelligent Computing Orchestration (LiCO) |
| -------------------------- | ----------------------------------------------- |
| Cluster Provisioning Tool  | Lenovo XClarity XCC2 server management controller. Lenovo-developed open-source software Confluent |
| Cluster Operating System   | Rocky Linux 9                                  |
| Dual Management Servers    | ThinkSystem SR665 V3. 48 core 2.5GHz AMD EPYC 9224 CPU, 256GB DDR5 RAM. Two 960GB & Two 6.4TB SSD. ConnectX-7 IB card. 10/25G ethernet NIC |
| Dual Login Servers         | ThinkSystem SR665 V3. 48 core 2.5GHz AMD EPYC 9224 CPU. 384GB DDR5 RAM. Two 960GB SSD & Two 6.4TB SSD. ConnectX-7 IB card. 10/25G ethernet NIC. |
| Compute Nodes(5)           | Think System SR665 V3. 64 core AMD EPYC 2.5GHz CPU, 768GB DDR5 RAM. Two 960GB SSD. Nvidia ConnectX-7 IB. Ethernet NIC. 10/25GB ethernet NIC. |
| NVIDIA GPU Ready Node(1)   | Think System SR675 V3. 48c AMD EPYC 9224 2.5GHz CPU. 768GB DDR5 Memory. NVIDIA ConnectX-7 IB. 6.4TB local disk OS Disk. |
| NVIDIA GPU Nodes-L40S(1)   | Think System SR675 V3 Node with 2 NVDIA L40s 48gb Gen4 GPUs. 48c AMD EPYC 9224 CPU & 768GB DDR5 Memory. ConnectX-7 IB. 6.4TB local disk & 960TB OS Disk. |
| NVIDIA GPU Nodes-H100(1)   | Think System SR675 V3 Node with 2 NVDIA H100 94GB Gen5 GPUs. 48c AMD EPYC 9224 CPU & 768GB DDR5 Memory. ConnectX-7 IB. 6.4TB local disk and 960TB OS Disk. |
| Total Compute Core         | 512                                           |
| Total Compute Memory       | 6144GB                                        |
| Total GPU Core             | Cuda = 26908 Tensor = 568                     |
| Total GPU Memory           | 284GB                                         |
| Network Interconnect       | 2 NVIDIA QM9700 64-Port Managed Quantum NDR InfiniBand Switch. NVIDIA SN2201 1GbE Managed switch for provision. NVIDIA SN2201 1GbE Managed switch for IPMI. |
| NAS Storage Servers(2)     | NVIDIA SR635 V3. 16c AMD EPYC 9124 3.0GHz CPU. NVIDIA ConnectX-7 IB. 384GB RDIMM-A Memory. Broadcom 100GBE CQSFP56 2-Port Ethernet Adapter. Lenovo External RAID 940-8e 12GB SAS card. Lenovo Internal RAID 5350-8i 12GB SAS |
| NAS JBOD(1)                | ThinkSystem D1212 Disk Exp Enclousre with six 3.5” 16TB disks. JBOD is attached to NAS Storage Servers. JBOD Volume is shared Between two Management Nodes which are in HA mode. |
| Storage System             | DDN EXAScaler 400NVX2 Appliance of 700TB Flash volume on Lustre parallel file system. HDR 200GbE Network. DDN SS9024 90-slot enclosure(2). 1.8TB volume of SAS Disk Cold tier used for HOME Directory, SMB, NFS, Backup. NSDS Protocol server used as file server for DDN SS9024 Enclosure. Dell Power Edge with 24c CPU, 128Gb Memory, ConnectX-6 IB Card with HDR100/100GbE Adapter. |

## Node Details


### PACC Compute Node

| Total Node | 5 |
| --- | --- |
| Nodes Type | Lenovo ThinkSystem SR645 V3 |
| Processor Type | AMD EPYC 9224 |
| Processor Speed | 2.5Hz |
| Number Of Socket | 2 |
| Cores Per Socket | 32 |
| Cores Per Node | 64 |
| Memory Size | 768GB |
| Memory Type | TruDDR5 4800MHz |
| Local Storage | 960GB NVMe Read Intensive SSD(2) |
| Network Storage(NFS) | /home{ext4} /project{lustre} /work{lustre} |
| Network InfiniBand Card | NVIDIA ConnectX-7 NDR200/200GbE |
| OS Type | Rocky Linux 9.3 |
| Production Date | March 2025 |

### PACC 2-way L40 GPU Node

| Total nodes | 1 |
| --- | --- |
| Nodes Type | Lenovo ThinkSystem SR675 V3 |
| Node Category | GPU |
| Processor Type | AMD EPYC 9224 @ 2.5Hz |
| Processor Details | Socket Number Core/Socket Core/Node |
| | 2 | 24 | 48 |
| Server Memory | 768GB TruDDR5 @ 4800MHz RDIMM-A |
| Local Disk Type | 6.4TB NVMe SSD (2) |
| OS Disk Type | 960GB NVMe Read Intensive SSD (2) |
| Network Interface Card | NVIDIA ConnectX-7 NDR200/200GbE 1GbE RJ45 4-Port Ethernet |
| OS Type | Rocky Linux 9.3 |
| NFS File System | /home (ext4) /project (Lustre) /scratch (Lustre) |
| GPU Per Node | 2 |
| GPU Type | NVIDIA L40s |
| Graphic Processor Name | AD102 |
| GPU Memory | 48GB GDDR6 384 bit 864 GB/s |
| Clock Speed | Base=1110MHz Boot=2520MHz |
| GPU Render Config | Shading Unit Tensor Core ROPS RT Cores TMUS L1 L2 SM-Count |
| | 18176 | 568 | 192 | 142 | 568 | 128KB 48MB 142 |
| Theoretical Performance | FP64 (double) FP32 (float) FR16 (half) Pixel Rate Texture Rate |
| | 1431 GFLOPS 91.6 TFLOPS 91.6 TFLOPS 483 Gpixel/s 1431 Gpixel/s |
| Delivery Date | April 2025 |

### PACC 2-Way H100 GPU Node

| Total nodes | 1 |
| --- | --- |
| Nodes Type | Lenovo ThinkSystem SR675 V3 |
| Node Category | GPU |
| Processor Type | AMD EPYC 9224 @ 2.5Hz |
| Processor Details | Socket Number Core/Socket Core/Node |
| | 2 | 24 | 48 |
| Server Memory | 768GB TruDDR5 @ 4800MHz RDIMM-A |
| Local Disk Type | 6.4TB NVMe SSD (2) |
| OS Disk Type | 960GB NVMe Read Intensive SSD (2) |
| Network Interface Card | NVIDIA ConnectX-7 NDR200/200GbE 1GbE RJ45 4-Port Ethernet |
| OS Type | Rocky Linux 9.3 |
| NFS File System | /home (ext4) /project (Lustre) /scratch (Lustre) |
| GPU Per Node | 2 |
| GPU Type | NVIDIA H100 |
| Graphic Processor Name | NVIDIA Hopper |
| GPU Memory | 94GB HBM3 6016 bit 3.9TB/s |
| Multi-Instance GPU(MIG) | Supported 7 MIGS @ 12GB each |
| Clock Speed | Base=1080MHz Boost=1785 MHz |
| Tensor Core | FP64 (double) FP32 (float) FR16 (half) FP8 |
| | 60 TFLOPS 835 TFLOPS 1671 TFLOPS 3341 TFLOPS |
| Delivery Date | April 2025 |

