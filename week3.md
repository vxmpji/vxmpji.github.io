# Week 3: Application Selection for Performance Testing

## Application Selection
For Week 3, I selected five applications representing different workload types to evaluate the Linux server's performance. 
CPU-intensive tests use `stress-ng` to generate high CPU load, while RAM-intensive tests use `stress-ng` to allocate memory. 
Disk I/O performance is tested with `dd`, simulating heavy read/write operations. 
Network-intensive tests use `wget` to download a large file, simulating network traffic. 
Finally, `nginx` is installed as a server application to observe performance under service conditions. 
These applications cover CPU, memory, disk, network, and service workloads to provide a comprehensive performance evaluation.

## Installation Evidence
The following screenshot shows the installation of all applications on the Ubuntu server using SSH:
![Installation](assets/week3_install.png)

## Expected Resource Profiles
| Application     | Expected CPU | Expected RAM | Expected Disk I/O | Expected Network |
|-----------------|-------------|-------------|-----------------|----------------|
| stress-ng CPU   | High        | Low         | Low             | None           |
| stress-ng RAM   | Medium      | High        | Low             | None           |
| dd I/O test     | Low         | Low         | High            | None           |
| wget test       | Low         | Low         | Low             | High           |
| nginx           | Medium      | Medium      | Medium          | Medium         |

## Monitoring Evidence
### CPU & RAM
![CPU & RAM](assets/week3_htop_cpu.png)
![RAM](assets/week3_htop_ram.png)

### Disk I/O
![Disk I/O](assets/week3_disk.png)

### Network
![Network](assets/week3_network.png)

### Server Application
![nginx](assets/week3_nginx.png)

## Monitoring Strategy
The monitoring strategy involves observing resource usage while each application runs. 
CPU and memory usage are tracked using `htop`. Disk I/O performance is measured with `iostat`. 
Network throughput is monitored during file transfers using `wget` or `iperf3`. 
Server application performance is verified via `systemctl status` and by checking response through a web browser. 
All monitoring commands are executed via SSH from the workstation, and screenshots are captured for documentation.
