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
- [Captures d'écran](#captures-ecran)
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
- Active Directory / ADCS
- DNS / DHCP
- OpenVPN
- Snort
- Squid
- Centreon
- Veeam Backup
- Nextcloud
- WDS / MDT
- Windows Admin Center

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
| Authorité de Certification | ADCS | Garantir l'authenticité des entités et garantir la confidentalité et l'intégrité des données échangées.
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

## <a id="sécurité-mise-en-œuvre"></a>🔒 Sécurité mise en œuvre

Plusieurs mécanismes de sécurité ont été mis en place afin de garantir la confidentialité, l'intégrité et la disponibilité des services.

### 🛡️ Segmentation réseau

L'infrastructure est organisée en plusieurs sous-réseaux distincts afin de séparer les différents périmètres et de limiter les mouvements latéraux en cas de compromission.

Les différents réseaux permettent notamment de distinguer :

- le réseau utilisateurs ;
- le réseau serveurs ;
- le réseau d'administration ;
- la DMZ ;
- le réseau WAN.

Cette séparation améliore la sécurité globale de l'infrastructure et facilite le contrôle des communications entre les différents services. 


---
### 🔥 Pare-feu et haute disponibilité

Deux pare-feux pfSense fonctionnent en haute disponibilité grâce au protocole CARP, Les états de connexion sont égalements synchronisés entre les pare-feux grâce au protocole pfSync.

Cette architecture permet :

- d'assurer la continuité de service ;
- d'éviter un point de défaillance unique ;
- de maintenir la disponibilité du réseau en cas de panne d'un pare-feu.
---
### 🌐 Accès distants sécurisés

Les connexions externes sont sécurisées grâce à OpenVPN.

Les accès distants permettent :

- l'administration des équipements ;
- l'accès aux ressources internes ;
- la protection des communications via le chiffrement.
---
### 🚨 Détection et prévention des intrusions

Snort est utilisé afin d'analyser le trafic réseau et détecter d'éventuelles activités malveillantes.

Fonctions assurées :

- analyse des paquets ;
- détection des signatures connues ;
- génération d'alertes ;
- prévention des attaques.
---
### 🌍 Filtrage Web

Squid permet de contrôler les flux HTTP et HTTPS.

Objectifs :

- filtrer les accès ;
- contrôler la navigation ;
- renforcer la sécurité des utilisateurs.
---
### 📦 Sauvegarde et continuité de service

Veeam Backup assure la protection des machines virtuelles et des données critiques.

Les sauvegardes permettent :

- la restauration rapide des services ;
- la limitation des pertes de données ;
- l'amélioration de la continuité d'activité.
---
### 📊 Supervision et alertes

Centreon permet de surveiller l'état des équipements et des services.

La supervision permet :

- de détecter rapidement les incidents ;
- d'être alerté en cas d'anomalie ;
- de garantir la disponibilité de l'infrastructure.
---
### 🌐 DMZ

Les services exposés sont isolés dans une zone démilitarisée (DMZ).

Cette séparation permet :

- de limiter l'exposition du réseau interne ;
- d'améliorer la sécurité globale ;
- de contrôler les flux entre les différents réseaux.
---
### 🔍 Analyse réseau

Wireshark et Tcpdump sont utilisés pour :

- l'analyse des trames ;
- le diagnostic réseau ;
- la résolution d'incidents ;
- la compréhension des flux entre les équipements.

---

## <a id="compétences-développées"></a>🧠 Compétences développées

Ce projet m'a permis de développer et d'approfondir plusieurs compétences dans les domaines des systèmes, des réseaux et de la cybersécurité.

| Domaine | Compétences acquises |
|-----------|-----------|
| 🖥️ Système | Installation et administration de Windows Server et Debian, Active Directory, DNS, DHCP, GPO |
| 🌐 Réseau | Plan d'adressage, routage, segmentation par sous-réseaux, règles de pare-feu, NAT |
| ☁️ Virtualisation | Déploiement et administration d'un environnement Proxmox |
| 🔥 Sécurité | pfSense, DMZ, OpenVPN, Snort, Squid, filtrage réseau, Certificat TLS |
| ♻️ Haute disponibilité | Mise en place de pfSense HA avec CARP |
| 📊 Supervision | Surveillance des équipements et services avec Centreon |
| 💾 Sauvegarde | Mise en œuvre de Veeam Backup et stratégies de restauration |
| 🚀 Déploiement | Déploiement automatisé de postes Windows avec MDT et WDS |
| 🔍 Diagnostic | Analyse du trafic réseau avec Wireshark et résolution d'incidents |
| 📚 Documentation | Réalisation de schémas, documentation technique et procédures d'administration |

### Objectifs pédagogiques

- Concevoir une infrastructure sécurisée proche d'un environnement professionnel ;
- Garantir la disponibilité des services ;
- Renforcer la sécurité du système d'information ;
- Développer des compétences en administration systèmes et réseaux ;
- Approfondir les concepts de cybersécurité et de continuité de service.

---

## <a id="captures-ecran"></a>📸 Captures d'écran

![🖥️Hyperviseur Proxmox](images/MENU_PROXMOX.png)


---
## <a id="état-du-projet"></a>🚀 État du projet                                         

Le projet est en cours de documentation.

