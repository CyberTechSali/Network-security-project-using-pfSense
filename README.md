# Network-security-project-using-pfSense
# 🔒 Network Security Project with pfSense

[![pfSense Version](https://img.shields.io/badge/pfSense-2.8.1-blue)](https://www.pfsense.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Snort](https://img.shields.io/badge/Snort-3.1.0-FF0000?logo=snort)](https://www.snort.org/)
[![OpenVPN](https://img.shields.io/badge/OpenVPN-2.6-32CD32?logo=openvpn)](https://openvpn.net/)

## 📖 Context
This end-of-studies project aims to deploy a secure enterprise network infrastructure using pfSense, integrating:

- ✅ Network segmentation (WAN/LAN/DMZ)
- ✅ Advanced firewall filtering rules
- ✅ Transparent proxy with web filtering (Squid + SquidGuard)
- ✅ Reverse proxy and load balancing (HAProxy)
- ✅ Intrusion detection/prevention system (Snort)
- ✅ Remote Access and Site-to-Site VPN (OpenVPN)
- ✅ Centralized certificate management (Internal PKI)

## 🏗️ Architecture
![Network Diagram](docs/network-diagram.png)

## 🚀 Implemented Features

### 1. Infrastructure Deployment
- pfSense installation on VMware VMs
- 3-interface configuration (WAN/LAN/DMZ)

### 2. Security Mechanisms
- **NAT & Port Forwarding**: Secure exposure of a web server in the DMZ
- **Firewall Rules**: "Deny by default" policy, restrictive DMZ→LAN rules
- **Access Control**: Internal CA creation to secure the Admin WebGUI

### 3. Service Security
- **Proxy (Squid)**: HTTPS filtering with SSL interception
- **SquidGuard**: Category-based blocking (University of Toulouse blacklist)
- **HAProxy**: HTTP/HTTPS load balancing

### 4. Intrusion Detection
- **Snort**: "Balanced" policy, effective detection of Nmap scans

### 5. Communication Security
- **OpenVPN Remote Access**: Certificate + User authentication
- **OpenVPN Site-to-Site**: Tunnel between two pfSense sites

## 📋 Prerequisites
- VMware Workstation / Player
- 2 pfSense VMs (or 1 + Windows/Linux client)
- Basic networking knowledge (subnets, routing)

## 🛠️ Quick Installation
1. Download the pfSense ISO
2. Create VMs with 3 network interfaces
3. Configure VMware virtual networks (Host-only)
4. Follow the step-by-step guide in [`docs/`](docs/)

## 🔧 Configuration Files
Full configuration export available in [`configs/`](configs/).

## 📸 Screenshots
See the [`docs/screenshots/`](docs/screenshots/) folder for detailed steps.

## 🎥 Demonstration
[![Demo Video](https://img.youtube.com/vi/.../0.jpg)](https://www.youtube.com/watch?v=...)

## 🧠 Lessons Learned
- ❌ **Error**: HTTPS filtering in "Bump" mode caused TLS errors.
- ✅ **Solution**: Switched to "Splice All" for whitelisted sites.
- 💡 **Best Practice**: Always separate CAs by usage (WebGUI vs VPN).

## 📚 Resources
- [Official pfSense Documentation](https://docs.netgate.com/pfsense/en/latest/)
- [SquidGuard Blacklist](https://dsi.ut-capitole.fr/blacklists/)

## 👤 Author
**Salma Ouchahed** - [GitHub](https://github.com/your-username) - [LinkedIn](https://linkedin.com/in/...)

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
