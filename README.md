# Projet-securite-reseau

## 📌 Présentation

Ce projet a été réalisé **en autonomie** dans le cadre de ma formation en **BUT Réseaux & Télécommunications** (parcours **Cybersécurité**). Il vise à **concevoir, configurer et sécuriser une architecture réseau virtualisée**, à l’aide de **pfSense**.

L’objectif principal est de **segmenter le réseau** en trois zones (LAN, DMZ, WAN), **configurer un pare-feu**, mettre en place un **serveur web dans la DMZ**, et **contrôler les flux réseau** à l’aide de règles de firewall et de NAT.

---

## 🧱 Architecture du lab

- **pfSense** en tant que pare-feu principal
- **3 interfaces réseau** :
  - `LAN` → Clients internes
  - `DMZ` → Serveur Web (Windows Server + IIS)
  - `WAN` → Accès Internet (bridge avec la carte physique)
- **Clients** : Windows 11 (LAN) et Windows Server 2022 (DMZ)

Un schéma réseau est disponible dans le rapport en pièce jointe.

---

## ⚙️ Fonctionnalités mises en place

### 🔧 Configuration réseau
- Installation de pfSense 2.7.2
- Affectation des interfaces LAN, DMZ, WAN
- Attribution d’adresses IP fixes

### 🔥 Règles de pare-feu
- Blocage du LAN → DMZ (protection contre pivoting)
- Autorisation spécifique du LAN → serveur web DMZ (port 80)
- Blocage total de la DMZ → LAN

### 🌐 Redirection de ports (NAT)
- Redirection WAN → serveur web en DMZ via port HTTP (TCP 80)
- Accès au site web depuis Internet simulé via l’interface WAN

---

## 👨‍💻 Auteur

**Yanis Horaira**  
Étudiant en BUT Réseaux & Télécommunications – IUT de Blagnac  
Parcours **Cybersécurité**

---

## 🛡️ Licence

Ce projet est mis à disposition à des fins pédagogiques et personnelles.  
Toute reproduction ou usage commercial sans autorisation est interdite.
