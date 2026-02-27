# 🏗️ Homelab AIS – Global Architecture Overview

## 1. Contexte

Ce homelab a été conçu dans le cadre de la formation Administrateur d’Infrastructures Sécurisées (AIS).

Il a pour objectif de reproduire une infrastructure d’entreprise réaliste intégrant :
- Virtualisation
- Segmentation réseau
- Services d’annuaire
- Supervision
- Sécurité
- Cloud privé

---

## 2. Objectifs du Lab

- Mettre en pratique les compétences du bloc 1, 2 et 3 du titre AIS
- Construire un environnement reproductible et documenté
- Simuler une infrastructure PME sécurisée
- Tester des scénarios d’attaque et de défense
- Préparer le Dossier Professionnel

---

## 3. Architecture Logique

L’infrastructure est organisée en plusieurs zones :

- LAN (réseau interne utilisateurs)
- DMZ (services exposés)
- Management Network
- Réseau de virtualisation

Le routage et le filtrage sont assurés par pfSense.

---

## 4. Stack Technique Globale

Hyperviseur :
- Proxmox VE

Firewall :
- pfSense

Services principaux :
- Active Directory
- DNS
- DHCP
- File Server
- VPN
- IDS/IPS (Suricata)
- Supervision (Wazuh / Zabbix)
- Cloud (OpenStack – lab académique)

---

## 5. Philosophie d’Architecture

Le lab est conçu selon les principes suivants :

- Segmentation réseau stricte
- Principe du moindre privilège
- Centralisation des logs
- Supervision proactive
- Documentation complète (GitHub)

---

## 6. Évolution Prévue

- Mise en place d’un SIEM complet
- Automatisation via scripts PowerShell / Bash
- Mise en place d’une stratégie de sauvegarde
- Infrastructure as Code
