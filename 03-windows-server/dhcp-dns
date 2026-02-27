# 🌐 – DNS & DHCP

## 🎯 Objectif

Mettre en place un serveur DHCP intégré à Active Directory afin de :

- Attribuer automatiquement les adresses IP
- Centraliser la gestion réseau
- Assurer l’enregistrement DNS dynamique
- Garantir la cohérence avec l’infrastructure AD

---

# 📦 Installation du rôle DHCP

Le rôle DHCP Server est installé via :

Server Manager → Add Roles and Features

Après installation, le serveur est :

- Autorisé dans Active Directory
- Vérifié comme opérationnel

---

## 🔐 Autorisation dans AD

Un serveur DHCP membre du domaine doit être autorisé dans Active Directory.

Cela permet :

- D’éviter les serveurs DHCP non autorisés
- De sécuriser l’attribution des adresses IP

---

# 🌍 Configuration du Scope

## 📌 Exemple de configuration

| Élément | Valeur |
|----------|--------|
| Réseau | 10.0.0.0 |
| Masque | 255.255.0.0 |
| Plage IP | 10.0.0.100 – 10.0.0.200 |
| Exclusions | 10.0.0.1 – 10.0.0.50 |
| Durée du bail | 8 jours |

---

## ⚙️ Options DHCP configurées

| Option | Valeur | Rôle |
|--------|--------|------|
| 003 Router | IP LAN pfSense | Passerelle |
| 006 DNS Server | IP du DC | Résolution interne |
| 015 DNS Domain Name | homelab.local | Domaine AD |

---

# 🔄 Intégration DNS Dynamique

Le serveur DHCP est configuré pour :

- Enregistrer automatiquement les clients dans DNS
- Mettre à jour les enregistrements A et PTR
- Nettoyer les enregistrements obsolètes

Cela garantit :

- Cohérence entre IP et DNS
- Résolution correcte des postes membres du domaine

---

# 🧪 Test de validation

Sur un poste client membre du domaine :

```
ipconfig /release
ipconfig /renew
```

Vérifications :

- Adresse IP reçue dans la plage définie
- DNS configuré vers le contrôleur de domaine
- Résolution fonctionnelle via :

```
nslookup nom_machine
```

---

# 🧠 Logique d’architecture

Dans cette infrastructure :

- pfSense assure le firewall et la segmentation
- Windows Server gère AD, DNS et DHCP
- Les postes clients utilisent exclusivement le DNS interne

Cette architecture permet :

- Une gestion centralisée
- Une cohérence réseau
- Une meilleure maîtrise des services Microsoft

---

# 📌 Conclusion

Le service DHCP est :

- Installé et autorisé dans AD
- Configuré avec un scope cohérent
- Intégré au DNS dynamique
- Testé et validé

Il complète l’infrastructure Active Directory et prépare la gestion des postes clients.
