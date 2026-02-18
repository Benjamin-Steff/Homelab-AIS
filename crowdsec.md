# CrowdSec – Protection & Détection

## 🎯 Objectif

Mettre en place une solution de détection comportementale afin d’identifier et bloquer automatiquement les activités malveillantes (bruteforce, scans réseau, tentatives d’intrusion) au sein de l’infrastructure.

---

## 🏗️ Architecture mise en place

- CrowdSec installé sur une machine Debian dédiée
- Collecte et analyse des logs système
- Bouncer configuré sur pfSense pour appliquer les décisions de blocage
- Communication entre CrowdSec et le firewall via API

Cette architecture permet de séparer la détection (analyse) de l’action (blocage).

---

## ⚙️ Fonctionnement

1. Les logs (SSH, système, services) sont analysés en temps réel.
2. CrowdSec détecte des comportements anormaux (ex : multiples tentatives de connexion échouées).
3. Une décision de bannissement est générée.
4. Le bouncer transmet cette décision au firewall.
5. L’adresse IP est automatiquement bloquée.

---

## 🛡️ Apport en sécurité

- Automatisation du blocage des attaques simples
- Réduction de la surface d’exposition
- Amélioration de la réactivité face aux scans automatisés
- Centralisation des décisions de sécurité

---

## 🚧 Évolutions prévues

- Mise en place du dashboard
- Tests d’attaque contrôlés pour valider l’efficacité
- Intégration dans une stratégie globale de monitoring
