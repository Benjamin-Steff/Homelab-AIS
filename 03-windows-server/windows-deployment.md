# Déploiement automatique via PXE (WDS + DHCP)

## 🎯 Objectif

Mettre en place un déploiement automatisé d’un système Windows via le réseau (PXE boot), sans support physique.

Le poste client démarre sur le réseau et récupère l’image d’installation depuis le serveur.

---

## 🏗 Infrastructure utilisée

Serveur : SRV-DC01  
Rôles installés :
- Active Directory
- DHCP
- Windows Deployment Services (WDS)

Réseau : 10.0.0.0/16

Stockage images : C:\RemoteInstall

---

## 🔄 Fonctionnement

1. Le client démarre en PXE
2. Requête DHCP envoyée
3. Attribution IP par le serveur DHCP
4. WDS répond à la requête PXE
5. Téléchargement image WinPE
6. Lancement installation Windows

---

## ⚙ Configuration réalisée

### DHCP
- Scope configuré
- Passerelle et DNS définis
- WDS et DHCP sur le même serveur

### WDS
- Intégré à Active Directory
- Dossier RemoteInstall sur volume dédié (D:)
- Import image Boot (WinPE)
- Import image Install (Windows ISO)

---

## 📀 Images utilisées

- Boot Image : WinPE issue de l’ISO Windows
- Install Image : Windows 10

---

## ✅ Résultat

- Déploiement réseau fonctionnel
- Installation Windows possible sans clé USB
- Infrastructure centralisée

---

## 🚧 Limites actuelles

- Aucun fichier unattended.xml configuré
- Installation semi-manuelle
- Pas de déploiement automatisé complet
- Pas de capture d’image personnalisée

---

## 🔮 Pistes d’amélioration

- Mise en place d’un fichier unattended.xml
- Automatisation complète de l’installation
- Intégration MDT (Microsoft Deployment Toolkit)
- Capture d’image personnalisée (Sysprep)
- Déploiement applicatif automatisé
- Segmentation PXE via VLAN

---

## 🧠 Compétences démontrées

- Interaction DHCP / PXE
- Configuration WDS
- Déploiement réseau d’OS
- Gestion d’infrastructure Windows
- Compréhension du boot réseau
