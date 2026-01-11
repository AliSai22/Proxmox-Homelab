# Cybersecurity Homelab (Proxmox)

## Overview
This project documents my personal cybersecurity homelab built to practice virtualization, Linux administration, networking, and basic penetration testing in a controlled environment.

The lab uses Proxmox VE as the main virtualization platform and runs multiple Linux virtual machines to simulate attacker–target scenarios. A custom Python-based Nmap automation tool is used for reconnaissance within the lab.

This setup is designed for learning, experimentation, and portfolio demonstration.

---

## Architecture

Host PC (Windows)
│
VMware Workstation
│
Proxmox VE (Virtual Server)
├─ Ubuntu Server VM (Target)
└─ Kali Linux VM (Attacker)



- **VMware** hosts Proxmox as a virtual server  
- **Proxmox VE** manages all nested virtual machines  
- **Ubuntu Server** acts as a target system  
- **Kali Linux** acts as the attacker system  

---

## Virtual Machines

### Proxmox VE
- Role: Virtualization platform
- Access: Web interface (`https://<proxmox-ip>:8006`)
- Manages all VMs and networking

### Ubuntu Server
- Role: Target machine
- Services: OpenSSH
- Purpose: Scan target for reconnaissance and testing

### Kali Linux
- Role: Attacker machine
- Tools:
  - Nmap
  - Python 3
- Purpose: Run reconnaissance and security tools

---

## Networking

- Proxmox uses a virtual bridge (`vmbr0`)
- Ubuntu and Kali VMs are on the same virtual network
- VMs can communicate with each other via internal IPs
- Host PC can access Proxmox Web UI through browser

---

## Tools Used

- VMware Workstation
- Proxmox VE
- Ubuntu Server
- Kali Linux
- Python 3
- Nmap

Custom tool:
- Python-based Nmap automation script  
  👉 *(linked in a separate repository)*

---

## Learning Outcomes

Through this project, I practiced:
- Setting up nested virtualization
- Managing VMs with Proxmox
- Linux installation and administration
- Virtual networking concepts
- Basic reconnaissance and scanning workflows
- Documenting technical projects for sharing

---

## Screenshots

Screenshots are available in the `screenshots/` directory:
- Proxmox Web Interface
- Kali Linux VM running
- Ubuntu Server VM running

---

## Future Improvements

- Add additional target VMs (web server, vulnerable apps)
- Expand Python scanning tool features
- Implement reporting and logging
- Add basic defensive monitoring

---

## Disclaimer

This lab is for **educational purposes only**.  
All testing is performed in a controlled environment on systems I own or am authorized to use.
