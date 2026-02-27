# 🖥️ 01 – Déploiement du Contrôleur de Domaine

## 🎯 Objectif

Déployer un contrôleur de domaine Windows Server au sein du homelab, intégré à une infrastructure virtualisée sous Proxmox et segmentée derrière un firewall pfSense.

L’objectif est d’obtenir une base stable pour :

- Active Directory
- DNS interne
- Authentification centralisée
- GPO
- Intégration RADIUS / VPN
- File Server

---

## 🧱 Contexte d’infrastructure

- Hyperviseur : Proxmox VE
- Firewall : pfSense
- Réseau : LAN interne isolé
- Aucun accès direct depuis le WAN
- Segmentation réseau via bridges Proxmox

Le serveur est positionné derrière pfSense sur le réseau interne.

---

## ⚙️ Paramètres de la Machine Virtuelle

| Paramètre | Valeur | Justification |
|------------|----------|---------------|
| vCPU | 2 | Suffisant pour un DC en environnement lab |
| RAM | 4 Go | AD + DNS + GPO stables |
| Disque | 60 Go | Espace pour SYSVOL, logs et évolutions |
| BIOS | UEFI | Compatibilité moderne |
| Carte réseau | Bridge LAN (ex: vmbr2) | Réseau interne sécurisé |
| Type disque | VirtIO | Performances optimisées |

---

## 🌐 Configuration réseau

Le serveur est configuré en IP statique.

| Élément | Configuration |
|----------|---------------|
| Adresse IP | 10.x.x.x |
| Masque | /16 ou /24 selon plan d’adressage |
| Passerelle | IP LAN pfSense |
| DNS primaire | Lui-même (après promotion DC) |

### 🔎 Choix technique

Un contrôleur de domaine doit impérativement :

- Utiliser une IP statique
- Pointer vers son propre service DNS
- Être isolé du WAN
- Être protégé par un firewall en amont

---

## 🔐 Configuration initiale post-installation

Après installation de l’OS :

- Renommage du serveur
- Mise à jour Windows
- Désactivation du compte invité
- Vérification du pare-feu Windows
- Attribution IP statique
- Installation des rôles nécessaires

---

## 🧠 Approche Architecture

Ce contrôleur de domaine :

- Fournit DNS interne
- Gère l’authentification centralisée
- Sert de base aux stratégies GPO
- Supporte la gestion des ACL sur le File Server

Il constitue la brique centrale de l’infrastructure interne.

---

## 🔎 Points de sécurité

- Pas d’exposition WAN directe
- Administration uniquement depuis le LAN
- Rôles limités au strict nécessaire
- Segmentation réseau assurée par pfSense

---

## 📌 Conclusion

Le déploiement a été réalisé en respectant :

- Les bonnes pratiques Microsoft
- Les principes de segmentation réseau
- Une logique d’architecture sécurisée
- Une cohérence avec le reste du homelab

Cette base permet ensuite :

- La promotion en contrôleur de domaine
- La structuration des OU
- La mise en place des groupes métiers
- Le déploiement de GPO
- L’intégration avec les services de sécurité
