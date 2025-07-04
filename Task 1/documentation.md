Task 1: Virtual Cybersecurity Lab Setup



🎯 Objective

To simulate a secure lab environment for cybersecurity testing using Virtual Machines (VMs) running on a host system, configured for internal communication, shared access, and basic security tool usage.



---



🖥️ Host System and Hypervisor



\- Host Operating System: Windows 10 x64 (Version: 22H2, Build: 10in1, ISO: ENU.OCT2022.ISO)

\- Hypervisor: Oracle VirtualBox Version 7.1.10 r169112 (Qt 6.5.3)



---



🧱 Virtual Machines Setup



| VM Name  | OS Version                           | ISO Used                              | RAM  | Storage | CPU | Role         |

|----------|---------------------------------------|--------------------------------------|------|---------|-----|--------------|

| Kali     | Kali Linux 2025.2                     | kali-linux-2025-2-release            | 4GB+ | 48GB+   | 2   | Attacker     |

| Windows  | Windows 10 Pro (x64)                  | W10X64.22H2.10in1.ENU.OCT2022.ISO    | 4GB+ | 50GB+   | 2   | Target       |

| pfsense  | pfSense-CE-2.6.0 amd64	           | pfSense-CE-2.6.0-RELEASE-amd64.iso   | 2GB+ | 16GB+   | 2   | firewall     |



---



🌐 Networking Configuration



VM configured  network adapters:



Adapter 1: internal network Adapter for internal communication between Kali, Windows, and pfsense VMs.

Adapter 2: NAT for internet access (for pfsense).



🔄 VM IP Address Mapping



| VM       | IP Address        |

|----------|-------------------|

| Windows  | 192.168.1.100      |

| Kali     | 192.168.1.103      |

| pfsense  | 192.168.1.1     |





✅ Ping Test Verification



\- Kali → Windows: Successful

\- Kali → pfsense: Successful

\- windows → kali: Successful

\- windows → pfsense: Successful


\- Screenshots of each ping test are included in the /screenshots/ folder.



---



📂 Shared Folder Configuration



VirtualBox Shared Folders were configured and verified on each VM:



\- Enabled auto-mount and read/write permissions

\- Tested visibility of shared content:

Kali: via `/media/sf\_Shared/`

Windows: as a mapped network drive





---



🛠 Tools Verified



\- ping – To verify inter-VM connectivity

\- ipconfig / ip a / ifconfig – To confirm VM IP addresses

\- nmap – To perform basic port scans (tested from Kali)

\- File Transfer – Verified shared folder access and file copying between VMs



---



🖼 Screenshots



Screenshots of the following have been saved to the `screenshots/` directory:



\- Kali Linux screenshots

\- Windows installation

\- pfsense screenshots

\- VirtualBox screenshots

\- Ping tests from Kali → Windows 

\- Shared folder access in Kali

\- service enumeration



---



🧪 Summary



All virtual machines have been configured correctly with internal communication and shared access. The lab simulates a basic real-world cybersecurity environment suitable for offensive and defensive testing in later tasks.



---


