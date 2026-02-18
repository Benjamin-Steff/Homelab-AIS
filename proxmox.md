# Proxmox – Installation & Configuration

## 🎯 Objectif
Mettre en place un hyperviseur Proxmox afin d’héberger une infrastructure virtualisée segmentée et sécurisée.

---

## 🖥️ Environnement matériel

- Serveur : Dell Precision 7810
- RAM : 16 Go (upgrade prévu)
- Stockage : SSD + HDD 
- Carte réseau : 1 interface physique

---

## 🌐 Configuration réseau

### Bridges configurés :

- **vmbr0** → WAN (connexion Internet)
- **vmbr1** → LAN interne
- **vmbr2** → Réseau VM isolé

Segmentation réalisée afin d’isoler :
- Le trafic Internet
- Le réseau interne
- Les machines virtuelles

---

## 🏗️ Machines virtuelles déployées

- Windows Server (Active Directory)
- Debian (services Linux)
- Machines clientes Windows

---

## 🔐 Sécurité

- Isolation des réseaux via pfSense
- Pas d’exposition directe des VM sur le WAN
- Accès administrateur restreint

---

## 🚧 Prochaines étapes

- Mise en place de sauvegardes (Proxmox Backup)
- Création de templates VM
- Monitoring de l’hôte
- Augmentation RAM
