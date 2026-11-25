# Linux Memory Forensics Using Volatility 3

## About
This is my beginner-level digital forensics project. I used Volatility 3 to examine a publicly available Linux memory image in an Ubuntu virtual machine.

## Objective
To learn how to identify Linux kernel information and analyze processes, process relationships, socket information and loaded kernel modules from a memory image.

## Tools
- Ubuntu Linux (VirtualBox)
- Python 3
- Volatility 3 Framework 2.28.2
- Linux symbol table matching the sample kernel

## Evidence
Public Linux training sample from the Volatility Foundation test-data repository.

Original source:
https://github.com/volatilityfoundation/volatility3-test-data

The extracted memory image was 512 MiB and contained a Debian Linux 3.2.0-4-amd64 kernel banner.

## Plugins Used
- `banners.Banners` — identified the kernel banner.
- `linux.pslist` — listed processes.
- `linux.pstree` — examined process relationships.
- `linux.sockstat` — examined socket information.
- `linux.lsmod` — listed loaded kernel modules.

## Findings
The analysis identified Linux kernel worker threads, local communication sockets and storage-related kernel modules.

These observations alone do not establish malicious activity.

## Learning Outcomes
- Learned how to install and configure Volatility 3.
- Learned why matching Linux symbols are important.
- Practiced basic Linux memory analysis.
- Learned to save plugin outputs and document findings.
- Practiced troubleshooting installation and symbol-related issues.

## Limitations
This was a beginner learning exercise using a historical public memory image. It was not a complete malware investigation or proof that the system was clean.

## Future Improvements
- Investigate suspicious processes and parent-child relationships.
- Explore additional Linux memory-forensics plugins.
- Correlate process and socket findings.
- Improve evidence documentation and reporting.

