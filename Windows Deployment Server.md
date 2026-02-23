# 🚀 Windows Deployment Services (WDS)

## 🎯 Objectif

Mettre en place un service de déploiement automatisé des postes clients via le réseau (PXE), afin de garantir :

- Une installation homogène des systèmes
- Une réduction du temps d’intervention
- Une standardisation des configurations
- Une intégration rapide au domaine Active Directory

---

## 🏗️ Architecture

Le service WDS est installé sur le contrôleur de domaine `SRV-DC01`.

L’infrastructure repose sur :

- Active Directory Domain Services (AD DS)
- DNS intégré à AD
- DHCP (attribution dynamique des adresses IP)
- WDS (déploiement PXE)

---

## 🔄 Fonctionnement du déploiement PXE

1. La machine cliente démarre en mode PXE
2. Elle obtient une adresse IP via DHCP
3. Le serveur WDS fournit l’image de démarrage (boot image)
4. L’image d’installation est téléchargée
5. Le système est installé automatiquement
6. Le poste est intégré au domaine Active Directory

---

## ⚙️ Configuration réalisée

- Installation du rôle **Windows Deployment Services**
- Configuration en mode intégré à Active Directory
- Ajout d’une image de démarrage (boot.wim)
- Ajout d’une image d’installation Windows
- Activation du démarrage PXE
- Autorisation des ordinateurs clients

---

## 🧠 Compétences démontrées

- Compréhension du mécanisme PXE
- Interaction DHCP / DNS / WDS
- Automatisation du déploiement de postes
- Intégration des machines au domaine
- Logique d’industrialisation d’un parc informatique

---

## 📌 Évolutions possibles

- Déploiement automatisé via fichiers de réponse (Unattended.xml)
- Intégration automatique à une OU spécifique
- Ajout de pilotes dans l’image WDS
- Déploiement d’applications post-installation
