# 🔒 Network Security Project with pfSense

[![pfSense Version](https://img.shields.io/badge/pfSense-2.8.1-blue)](https://www.pfsense.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Report Language](https://img.shields.io/badge/Report-Language_French-blue?label=Report%20Language&color=blue)](docs/)

---

## 📖 Overview

This project, completed as part of my academic training, focuses on deploying a **secure enterprise network infrastructure** using **pfSense**. The goal was to implement a **defense-in-depth** strategy to protect corporate assets against modern cyber threats.

The full technical documentation, including all installation steps, configuration details, and screenshots, is available in the attached PDF report.

> **📄 Note**: The comprehensive project report is written in **French (Français)**.  
> *Le rapport détaillé du projet est rédigé en **Français**.*

---

## 🏗️ Implemented Architecture & Features

- **3-Zone Network Segmentation** : WAN (External), LAN (Internal), DMZ (Exposed Servers).
- **Firewall & Filtering** : Strict "Deny by Default" policy with restrictive rules (especially blocking DMZ → LAN traffic).
- **NAT & Port Forwarding** : Secure exposure of internal web services via the DMZ.
- **Transparent Proxy & Web Filtering** : Squid in transparent mode, combined with SquidGuard for category-based blocking using the University of Toulouse blacklist.
- **Reverse Proxy & Load Balancing** : HAProxy configured for HTTP/HTTPS traffic distribution.
- **Intrusion Detection / Prevention (IDS/IPS)** : Snort deployed in IPS mode with a "Balanced" policy (successfully detecting Nmap scans).
- **Secure Communications (VPN)** :
  - **Remote Access VPN** : OpenVPN with two-factor authentication (Certificate + User/Password).
  - **Site-to-Site VPN** : OpenVPN tunnel established between two pfSense sites.
- **Internal Public Key Infrastructure (PKI)** : Creation of a dedicated internal Certificate Authority (CA) used to secure the WebGUI, SSL interception, and VPN tunnels.

---

## 📂 Repository Content
