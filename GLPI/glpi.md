# GLPI – Gestion de parc et support IT

## Présentation

**GLPI** est une solution open source de gestion des services informatiques (ITSM).  
Elle permet de centraliser la gestion d’un parc informatique, le support utilisateur et le suivi des incidents via un système de tickets.

Dans un environnement professionnel, GLPI est souvent utilisé pour :

- gérer les **tickets de support**
- suivre les **incidents** et les **demandes utilisateurs**
- inventorier le **parc informatique**
- centraliser les **utilisateurs** et les **équipements**
- améliorer le **suivi** et la **traçabilité** des interventions

GLPI peut également s’intégrer à un annuaire **LDAP / Active Directory** afin de réutiliser les comptes existants de l’infrastructure.

---

## Intégration dans le homelab

Dans ce homelab, GLPI a été déployé pour simuler un **outil de support IT d’entreprise**.  
L’objectif n’était pas de construire une plateforme ITSM complète, mais d’ajouter une brique réaliste de **gestion des incidents** et de **support utilisateur** à l’infrastructure existante.

Cette intégration permet de compléter l’environnement déjà en place autour de :

- **Windows Server**
- **Active Directory**
- **services web internes**
- **gestion des utilisateurs**

GLPI apporte ainsi une dimension plus opérationnelle au lab, en reproduisant un usage concret que l’on retrouve dans de nombreuses organisations.

---

## Intérêt de GLPI dans le lab

L’ajout de GLPI dans le homelab permet de :

- simuler un **helpdesk interne**
- centraliser les **demandes utilisateurs**
- suivre les **tickets d’incident**
- associer les demandes à des **utilisateurs**
- illustrer l’usage d’un **outil ITSM** dans une infrastructure d’entreprise

Même dans une version simple, cela permet de montrer que le lab ne se limite pas à l’administration système pure, mais intègre aussi une partie **gestion du support** et **organisation des interventions**.

---

## Captures

### Interface d’installation

![Installation GLPI](glpi.png)

### Exemple de ticket

![Ticket GLPI](Ticket-test.png)

### Ajout / synchronisation d’utilisateurs

![Synchronisation utilisateurs GLPI](glpi-synchro-user.png)

---

## Documentation d’installation

La procédure officielle d’installation de GLPI est disponible ici :  
[Documentation officielle GLPI](https://help.glpi-project.org/tutorials/fr/procedures/install_glpi)

---

## Conclusion

GLPI ajoute au homelab une composante orientée **support**, **suivi des incidents** et **gestion des utilisateurs**.  
C’est une solution pertinente pour illustrer un environnement IT plus proche d’un contexte professionnel, en complément des services d’infrastructure déjà déployés.
