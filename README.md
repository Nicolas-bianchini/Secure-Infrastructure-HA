# 🏗 Infrastructure sécurisée haute disponibilité

Architecture réseau segmentée et virtualisée intégrant firewall en haute disponibilité (CARP), accès VPN sécurisé, proxy web, services isolés en DMZ et détection d'intrusion.

---

## 📌 Présentation

Ce projet vise à simuler une infrastructure PME sécurisée reposant sur des bonnes pratiques réseau, systèmes et sécurité.

---

## 🎯 Objectifs

- Concevoir une architecture segmentée
- Implémenter un firewall en haute disponibilité (CARP)
- Assurer la continuité de service
- Mettre en place un accès distant sécurisé (VPN)
- Mettre en œuvre des contrôles de sécurité réseau
- Superviser et sauvegarder l’infrastructure
- Documenter l’ensemble de l’infrastructure

---

## 🏗 Architecture technique

### 🔥 Couche réseau
- Firewall HA (CARP) avec synchronisation des états
- Segmentation réseau via bridges virtuels
- Filtrage inter-réseau
- NAT

### 🖥 Couche infrastructure
- Hyperviseur : Proxmox
- Active Directory en redondance
- DNS & DHCP en redondance
- Segmentation des services (LAN_SERVER / LAN_USER / ADMIN)
  
### 🌐 DMZ
- Service collaboratif (Nextcloud)

  ---

## 🛡 Contrôles de sécurité

### 🔥 Filtrage & segmentation
- Règles firewall inter-réseau
- Isolation DMZ

### 🌍 Contrôle des flux sortants
- Proxy Squid (filtrage web)

### 🚨 Détection d’intrusion
- Snort (IDS/IPS)

### 🔐 Accès distant
- VPN OpenVPN sécurisé

---

## 💾 Supervision & continuité

- Sauvegarde via Veeam
- Supervision via Centreon

---

## 🧠 Compétences développées

| Domaine | Compétences |
|----------|------------|
| Architecture réseau | Segmentation, isolation DMZ |
| Haute disponibilité | CARP, basculement |
| Administration systèmes | AD, GPO, DNS, DHCP |
| Sécurité | Firewalling, Proxy, IDS/IPS |
| Virtualisation | Proxmox |
| Continuité | Sauvegarde & supervision |

---

## 🛠 Technologies utilisées

Windows Server · Active Directory · pfSense · OpenVPN · Squid · Snort · Proxmox · Veeam · Centreon · Windows Admin Center · Cockpit
  
## 🚀 Évolutions possibles

- Centralisation des logs (SIEM)
- Durcissement avancé des serveurs
- Automatisation PowerShell

