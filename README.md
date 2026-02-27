# 🧱 Homelab – Infrastructure & Sécurité

Infrastructure virtualisée reproduisant l’architecture d’une PME sécurisée.
Projet réalisé dans le cadre de la formation Administrateur d’Infrastructures Sécurisées (AIS).

---

## 🎯 Objectif du projet

Ce homelab a pour but de :

- Concevoir une infrastructure complète virtualisée
- Mettre en œuvre une segmentation réseau sécurisée
- Déployer un Active Directory fonctionnel
- Implémenter des mécanismes de détection d’intrusion
- Documenter chaque étape de manière professionnelle

L’ensemble du projet est structuré comme une infrastructure d’entreprise réelle.

---

## 🏗️ Architecture globale

- Hyperviseur : **Proxmox VE**
- Firewall : **pfSense**
- Segmentation LAN / zones sécurisées
- Active Directory (Windows Server)
- Postes clients Windows
- Services Linux (Debian)
- Détection d’intrusion (CrowdSec)
- Scripts d’automatisation (Python)

---

## 🔐 Sécurité implémentée

- Segmentation réseau via firewall
- Filtrage inter-réseaux
- Détection et blocage d’attaques
- Gestion des droits via Active Directory
- Centralisation progressive des services

---

## 📂 Documentation technique

La documentation détaillée est disponible dans les dossiers :

- `01-architecture`
- `02-network`
- `03-active-directory`
- `04-security`
- `05-services`

Chaque composant est documenté avec :
- Schémas
- Choix techniques
- Justifications d’architecture

---

## 🔹 Projet complémentaire

### Subnet Calculator (Python)
Outil graphique permettant le calcul de sous-réseaux IPv4  
👉 https://github.com/istare-cyber/Subnet-calculator

---

## 🚀 Roadmap

- Mise en place d’une stratégie de sauvegarde
- Monitoring & supervision
- Durcissement avancé
- Automatisation des déploiements

---

## 📌 Objectif professionnel

Administrateur systèmes & réseaux en évolution vers des environnements sécurisés.

Ouvert à :
- Stage
- CDD
- CDI

Mobile géographiquement.
