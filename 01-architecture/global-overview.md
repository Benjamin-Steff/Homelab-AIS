# 🏗️ Homelab AIS – Global Architecture Overview

## 1. Contexte

Ce homelab a été conçu dans le cadre de la formation 
Administrateur d’Infrastructures Sécurisées (AIS).

L’objectif est de reproduire une infrastructure PME sécurisée 
permettant de mettre en œuvre les compétences techniques 
attendues d’un administrateur systèmes et réseaux.

---

## 2. Objectifs du Lab

- Mettre en pratique les compétences des blocs 1, 2 et 3 du titre AIS
- Construire un environnement reproductible et documenté
- Simuler une infrastructure d’entreprise segmentée
- Tester des scénarios d’attaque et de défense
- Préparer le Dossier Professionnel

---

## 3. Architecture Logique

L’infrastructure est organisée en plusieurs zones :

- **WAN** (connexion via Box FAI – réseau 192.168.x.0/24)
- **LAN** (réseau interne 10.0.0.0/16)
- **DMZ** (services exposés)
- **Management Network**
- **Réseau de virtualisation**

Le routage, le NAT et le filtrage sont assurés par pfSense.

---

## 4. Stack Technique Globale

### Hyperviseur
- Proxmox VE (KVM)

### Firewall
- pfSense

### Services principaux
- Active Directory (Windows Server)
- DNS / DHCP
- File Server
- VPN (Client-to-Site)
- IDS/IPS (Suricata)
- Supervision (Wazuh / Zabbix)
- Cloud (OpenStack – environnement académique)

---

## 5. Principes d’Architecture

Le lab est conçu selon les principes suivants :

- Segmentation réseau stricte
- Principe du moindre privilège
- Cloisonnement des services
- Centralisation et analyse des logs
- Supervision proactive
- Documentation complète et versionnée (GitHub)

---

## 6. Évolutions Prévues

- Mise en place d’un SIEM complet
- Automatisation (PowerShell / Bash)
- Stratégie de sauvegarde et PRA
- Infrastructure as Code (Ansible / Terraform)
