# 🔒 Projet de sécurisation réseau avec pfSense

[![pfSense Version](https://img.shields.io/badge/pfSense-2.8.1-blue)](https://www.pfsense.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📖 Contexte
Ce projet, réalisé dans le cadre de ma formation, consiste à déployer une infrastructure réseau sécurisée en utilisant **pfSense**. L'objectif est de mettre en place une défense en profondeur (segmentation, pare-feu, proxy, IDS/IPS, VPN) pour protéger un réseau d'entreprise.

## 🏗️ Architecture mise en place
- **Segmentation en 3 zones** : WAN (externe), LAN (interne), DMZ (serveurs exposés).
- **Pare-feu** : Politique "deny by default" avec règles restrictives (notamment DMZ → LAN).
- **Proxy & Filtrage** : Squid en mode transparent, couplé à SquidGuard pour le blocage par catégories (blacklist Université de Toulouse).
- **Détection d'intrusions** : Snort en mode IPS avec politique "Balanced" (détection efficace de scans Nmap).
- **VPN** : OpenVPN en accès distant (certificat + mot de passe) et en Site-à-Site.
- **PKI interne** : Création d'une Autorité de Certification (CA) pour sécuriser l'interface Web, l'interception SSL et les tunnels VPN.

## 📂 Contenu du dépôt
- [`docs/Projet_Securisation_pfSense.pdf`](docs/Projet_Securisation_pfSense.pdf) : Rapport complet au format PDF, contenant toutes les étapes d'installation, les captures d'écran et les justifications techniques.
- `LICENSE` : Licence du projet (MIT).

## 🚀 Pourquoi ce projet est intéressant ?
- **Approche exhaustive** : Couvre la majorité des briques de sécurité d'un réseau d'entreprise.
- **Gestion des erreurs documentée** : Le rapport montre les problèmes rencontrés (notamment sur l'interception HTTPS) et les solutions apportées, démontrant une vraie capacité d'analyse.
- **Cohérence cryptographique** : Utilisation d'une même infrastructure à clés (PKI) pour plusieurs services.

## 🛠️ Prérequis pour reproduire le projet
- VMware Workstation / VirtualBox
- 2 machines virtuelles pfSense (ou 1 pfSense + 1 client Windows/Linux)
- Connaissances en réseau (sous-réseaux, routage)

## 📖 Comment lire ce projet ?
1. Téléchargez le fichier PDF dans le dossier `docs/`.
2. Suivez les chapitres dans l'ordre : de l'installation initiale à la mise en place des VPN.
3. Les captures d'écran illustrent chaque étape clé.

## 👤 Auteur
**Salma Ouchahed**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin)](https://linkedin.com/in/votre-profil) 
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github)](https://github.com/votre-compte)

## 📜 Licence
Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.
