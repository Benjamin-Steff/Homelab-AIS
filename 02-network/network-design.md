# 🌐 Network Design

## 1. Vue d’ensemble

L’infrastructure réseau du homelab est structurée autour d’un firewall pfSense jouant le rôle de point central de routage et de filtrage.

Le lab est connecté au réseau domestique, mais les environnements internes sont isolés via segmentation logique.

---

## 2. Topologie générale

### Réseau domestique
- 192.168.X.0/24
- Connexion à Internet via box FAI
- Proxmox connecté sur ce réseau (vmbr0)

### Firewall pfSense

Interfaces configurées :

- WAN : 192.168.x.254/24 (connecté au réseau domestique)
- LAN 1 : 10.0.0.1/16
- LAN 2 : 172.16.0.1/16

pfSense assure :
- Routage inter-réseaux
- NAT sortant vers Internet
- Attribution DHCP pour les réseaux internes

---

## 3. Segmentation interne

| Zone   | Plage IP        | Rôle |
|--------|----------------|------|
| WAN    | 192.168.x.0/24 | Accès vers réseau domestique |
| LAN 1  | 10.0.0.0/16     | Réseau interne principal |
| LAN 2  | 172.16.0.0/16   | Réseau interne secondaire |

Chaque réseau interne est isolé et contrôlé par pfSense.

---

## 4. Principe de sécurité

- Les réseaux internes ne communiquent qu’à travers pfSense
- Le NAT est utilisé pour l’accès Internet
- La segmentation limite les déplacements latéraux
- Les services DHCP sont séparés par segment

---

## 5. Évolution prévue

- Transformation du LAN 2 en DMZ dédiée
- Mise en place de règles de filtrage inter-segments strictes
- Ajout d’un réseau Management isolé
