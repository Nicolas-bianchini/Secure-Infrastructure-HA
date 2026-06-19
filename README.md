# 🏗 Infrastructure sécurisée haute disponibilité

Projet d’infrastructure sécurisée et hautement disponible, réalisé dans le cadre de mon BTS SIO option SISR.

L'objectif est de concevoir une architecture proche d'un environnement professionnel en intégrant la virtualisation, la segmentation réseau, la haute disponibilité, la supervision, les sauvegardes et plusieurs mécanismes de sécurité.

Ce projet me permet d'approfondir les domaines suivants :

- Administration systèmes Windows Server et Debian ;
- Virtualisation avec Proxmox ;
- Pare-feu et routage avec pfSense ;
- Active Directory, DNS et DHCP ;
- VPN et accès distants sécurisés ;
- Segmentation réseau ;
- Détection d'intrusion ;
- Supervision et surveillance ;
- Sauvegarde et continuité de service.
---

## Sommaire
- [Objectif](#objectif)
- [Technologies utilisées](#technologies-utilisees)
- [Architecture](#architecture)
- [Services déployés](#services-déployés)
- [Sécurité mise en œuvre](#sécurité-mise-en-œuvre)
- [Compétences développées](#compétences-développées)
- [État du projet](#état-du-projet)

---

## <a id="objectif"></a>🎯 Objectif

Concevoir une infrastructure complète simulant un environnement professionnel avec :

- haute disponibilité ;
- segmentation réseau ;
- services Windows Server ;
- accès distant sécurisé ;
- supervision ;
- sauvegarde ;
- sécurité réseau.

---

## <a id="technologies-utilisees"></a>🛠️ Technologies utilisées

- Proxmox
- pfSense
- CARP
- Active Directory
- DNS / DHCP
- OpenVPN
- Snort
- Squid
- Centreon
- Veeam Backup
- Nextcloud
- WDS / MDT

---

## <a id="architecture"></a>🏗️ Architecture

L'infrastructure est basée sur un hyperviseur Proxmox hébergeant plusieurs machines virtuelles réparties dans différents réseaux segmentés.

L'objectif est de reproduire une infrastructure professionnelle intégrant :

- La haute disponibilité ;
- La segmentation réseau ;
- L'administration centralisée ;
- La supervision ;
- Les sauvegardes ;
- La sécurité des accès ;
- L'exposition contrôlée de services.

### Schéma d'architecture

![Architecture globale](images/Plateformes_Schéma.png)

### Principales caractéristiques

- Virtualisation avec Proxmox ;
- Haute disponibilité des pare-feux ;
- Segmentation réseau par sous-réseaux ;
- Administration centralisée via Active Directory ;
- VPN pour les accès distants sécurisés ;
- Détection d'intrusion ;
- Supervision de l'infrastructure ;
- Sauvegardes des services critiques ;
- Exposition contrôlée des services via une DMZ.


---

## <a id="services-déployés"></a>🖥️ Services déployés

L'infrastructure intègre plusieurs services permettant de garantir la disponibilité, la sécurité et l'administration centralisée du système d'information.

| Service | Technologie | Rôle |
|-----------|------------|------|
| Hyperviseur | Proxmox VE | Hébergement et gestion des machines virtuelles |
| Pare-feu | pfSense | Filtrage, routage et sécurisation des flux |
| Haute disponibilité | CARP | Continuité de service des pare-feux |
| Annuaire | Active Directory | Authentification centralisée des utilisateurs |
| DNS | Windows Server | Résolution de noms |
| DHCP | Windows Server | Attribution automatique des adresses IP |
| VPN | OpenVPN | Accès distant sécurisé |
| IDS / IPS | Snort | Détection et prévention des intrusions |
| Proxy | Squid | Contrôle et filtrage du trafic web |
| Supervision | Centreon | Surveillance de l'infrastructure |
| Sauvegarde | Veeam Backup | Protection et restauration des données |
| Service collaboratif | Nextcloud | Partage et stockage de fichiers |
| Déploiement | MDT / WDS | Installation automatisée des postes |
| Analyse réseau | Wireshark / Tcpdump | Analyse et diagnostic du trafic |
| Administration distante | Windows Admin Center / SSH / RSAT | Gestion des serveurs |
| DMZ | Réseau isolé | Hébergement des services exposés |


### Fonctionnalités mises en œuvre

✅ Haute disponibilité des pare-feux avec CARP

✅ Segmentation réseau

✅ Authentification centralisée avec Active Directory

✅ Services DNS et DHCP

✅ VPN sécurisé pour les accès distants

✅ Détection et prévention des intrusions

✅ Filtrage du trafic Web

✅ Supervision de l'infrastructure avec alertes

✅ Sauvegarde et restauration des services critiques

✅ Déploiement automatisé des postes Windows

✅ Exposition contrôlée de services en DMZ

✅ Analyse et diagnostic réseau


---

## <a id="état-du-projet"></a>🚀 État du projet                                         

Le projet est en cours de documentation.

