# 🖥️ Hyper-V Virtualisation

## Présentation

Hyper-V est l’hyperviseur de virtualisation développé par Microsoft et intégré à **Windows Server**.

Il permet de créer et administrer des **machines virtuelles (VM)** afin d’héberger plusieurs services sur un même serveur physique.

Hyper-V est un **hyperviseur de type 1 (bare-metal)** : il fonctionne directement sur le matériel, ce qui permet de meilleures performances et une isolation efficace entre les machines virtuelles.

Dans une infrastructure professionnelle, il est souvent utilisé pour héberger des services comme :

- Active Directory
- DHCP
- File Server
- Web Server
- Applications métiers

---

## Concepts principaux

Une infrastructure Hyper-V repose sur plusieurs éléments.

### Hôte Hyper-V

Serveur physique exécutant le rôle **Hyper-V** et hébergeant les machines virtuelles.

### Machines virtuelles

Chaque machine virtuelle possède ses propres ressources :

- CPU virtuels
- mémoire RAM
- disque virtuel
- interface réseau virtuelle

Chaque VM fonctionne comme un système indépendant.

---

## Réseau virtuel

Hyper-V permet de créer des **commutateurs virtuels (Virtual Switches)** pour connecter les machines virtuelles.

Types de commutateurs disponibles :

- **External** : accès au réseau physique et à Internet  
- **Internal** : communication entre l’hôte et les VM  
- **Private** : communication uniquement entre VM

---

## Utilisation en entreprise

Dans les infrastructures professionnelles, Hyper-V permet :

- la consolidation des serveurs
- l’optimisation des ressources matérielles
- la simplification du déploiement de services
- l’amélioration de la maintenance et des sauvegardes

Certaines fonctionnalités permettent également d’améliorer la disponibilité :

- **Live Migration**
- **Failover Clustering**
- **sauvegarde des machines virtuelles**

---

## Utilisation dans ce homelab

Dans ce homelab, Hyper-V est principalement utilisé à des fins **d’apprentissage et de compréhension de la virtualisation dans l’écosystème Microsoft**.

L’infrastructure principale du lab repose cependant sur **Proxmox**, utilisé comme hyperviseur principal.

Hyper-V est donc présenté ici pour compléter la documentation autour des technologies de virtualisation utilisées dans les environnements Windows Server.
