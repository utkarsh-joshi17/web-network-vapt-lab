# Phase 1: Lab Setup

## Objective
Build an isolated penetration testing lab.

## Environment
| Machine | Role | OS | IP |
|---|---|---|---|
| Kali Linux 2026.3 | Attacker | Debian 64-bit | 192.168.44.x |
| Metasploitable 2 | Target (network) | Ubuntu 8.04 | 192.168.44.3 |
| OWASP Juice Shop | Target (web) | Docker on Kali | localhost:3000 |

## Network
- Hypervisor: VirtualBox
- Kali: Adapter 1 NAT, Adapter 2 Host-only (#2)
- Metasploitable: Host-only only (#2), isolated from the internet
- DHCP range: 192.168.44.3 – 192.168.44.254

## Steps
1. Installed VirtualBox ![](screenshots/01-virtualbox-version.png.png)
2. Configured host-only network + DHCP ![](screenshots/02-host-only-dhcp.png.png)
3. Imported Kali, set network adapters ![](screenshots/03-kali-network-adapters.png.png)
4. Created Metasploitable VM, obtained IP ![](screenshots/04-matasploitable-ifconfig.png.png)
5. Deployed Juice Shop with Docker ![](screenshots/05-juice-shop-running.png.png)
6. Verified connectivity ![](screenshots/06-kali-ping-metasploitable.png.png)
7. Baseline Nmap scan ![](screenshots/07-nmap-baseline.png.png)
