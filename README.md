# 🔒 Network Security Project with pfSense

[![pfSense Version](https://img.shields.io/badge/pfSense-2.8.1-blue)](https://www.pfsense.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📖 Context
This project, carried out as part of my academic training, aims to deploy a secure network infrastructure using **pfSense**. The objective is to implement a defense-in-depth strategy (segmentation, firewall, proxy, IDS/IPS, VPN) to protect an enterprise network.

## 🏗️ Implemented Architecture
- **3-Zone Segmentation** : WAN (external), LAN (internal), DMZ (exposed servers).
- **Firewall** : "Deny by default" policy with restrictive rules (notably DMZ → LAN).
- **Proxy & Filtering** : Squid in transparent mode, coupled with SquidGuard for category-based blocking (University of Toulouse blacklist).
- **Intrusion Detection** : Snort in IPS mode with a "Balanced" policy (effective detection of Nmap scans).
- **VPN** : OpenVPN for remote access (certificate + password) and Site-to-Site.
- **Internal PKI** : Creation of a Certificate Authority (CA) to secure the Web interface, SSL interception, and VPN tunnels.

## 📂 Repository Content
- [`docs/Projet_Securisation_pfSense.pdf`](docs/Projet_Securisation_pfSense.pdf) : Complete PDF report, containing all installation steps, screenshots, and technical justifications.
- `LICENSE` : Project license (MIT).

## 🚀 Why This Project is Interesting
- **Comprehensive Approach** : Covers the majority of security building blocks for an enterprise network.
- **Documented Error Handling** : The report shows the issues encountered (notably regarding HTTPS interception) and the solutions implemented, demonstrating strong analytical skills.
- **Cryptographic Consistency** : Use of the same PKI infrastructure across multiple services.

## 🛠️ Prerequisites to Reproduce This Project
- VMware Workstation / VirtualBox
- 2 pfSense virtual machines (or 1 pfSense + 1 Windows/Linux client)
- Basic networking knowledge (subnets, routing)

## 📖 How to Read This Project
1. Download the PDF file from the `docs/` folder.
2. Follow the chapters in order: from the initial installation to the VPN setup.
3. The screenshots illustrate each key step.

## 👤 Author
**Salma Ouchahed**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin)](https://linkedin.com/in/your-profile) 
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github)](https://github.com/your-username)

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
