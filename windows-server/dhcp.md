# 📦 Mise en place du serveur DHCP
## 🎯 Objectif

Mettre en place un serveur DHCP centralisé sur le contrôleur de domaine afin de :

- Distribuer automatiquement des adresses IP aux postes clients  
- Fournir les paramètres réseau nécessaires (passerelle, DNS, domaine)  
- Préparer l’environnement pour le déploiement PXE via WDS  

---

## 🖥️ Contexte d’infrastructure

- **Domaine** : `home.lab`  
- **Contrôleur de domaine** : Windows Server  
- **Réseau interne** : `10.x.x.x/16`  
- **Pare-feu / passerelle** : pfSense  

Le rôle DHCP est installé sur le contrôleur de domaine afin de centraliser la gestion réseau dans l’environnement Active Directory.

---

## ⚙️ Installation du rôle DHCP

1. Ajout du rôle **DHCP Server** via le Gestionnaire de serveur  
2. Autorisation du serveur DHCP dans Active Directory  
3. Vérification du bon démarrage du service  

---

## 🌐 Configuration de l’étendue IPv4

Une plage dynamique est configurée dans le réseau privé `10.x.x.x/16`.

Les adresses utilisées par l’infrastructure (serveur, pare-feu, etc.) sont exclues de la distribution automatique afin d’éviter tout conflit IP.

---

## 🧩 Options d’étendue configurées

Les options suivantes sont définies :

- **Routeur (003)** : adresse de la passerelle réseau  
- **Serveur DNS (006)** : adresse du contrôleur de domaine  
- **Nom de domaine (015)** : `home.lab`  
- **PXEClient (060)** : activé pour l’intégration avec WDS  

> Les options 66 et 67 ne sont pas configurées manuellement car DHCP et WDS sont hébergés sur le même serveur.

---

## 🚀 Intégration avec WDS

Le serveur DHCP permet :

1. L’attribution automatique d’une adresse IP lors du démarrage PXE  
2. La transmission des informations nécessaires au boot réseau  
3. L’intégration native avec Windows Deployment Services  

---

## 🧠 Bonnes pratiques appliquées

- IP fixe pour le contrôleur de domaine  
- Plage DHCP distincte des adresses d’infrastructure  
- Centralisation DNS sur le serveur AD  
- Séparation des rôles : pare-feu (pfSense) / services Windows  

---

## 📌 Résultat

Le serveur DHCP fonctionne correctement et prépare l’environnement pour le déploiement automatisé des postes via WDS.
