# 🔐 Rogue DHCP Attack Detection

## 🎯 Objectif
Simulation d’une attaque **Rogue DHCP** afin de comprendre son fonctionnement et mettre en place des méthodes de **détection réseau**.

---

##  Contexte
Un Rogue DHCP est un serveur DHCP non autorisé qui distribue de fausses configurations réseau.

 **Risques** :
- Interception du trafic (**MITM**)
- Redirection DNS
- Perte de connectivité
- Compromission du réseau

---

##  Environnement

- Kali Linux (attaquant)
- Machine Windows (serveur DHCP légitime)
- Machine Windows (client)
- Réseau local (lab)

---

##  Outils

- Yersinia (attaque DHCP)
- Tftpd32 (serveur DHCP)
- Commandes réseau :
  - `ipconfig /all`
  - `arp -a`
- DHCPLOC (outil de détection)

---

##  Scénario d’attaque

1. Mise en place d’un serveur DHCP légitime  
2. Saturation des baux (**DHCP Starvation**)  
3. Déploiement d’un serveur DHCP malveillant  
4. Attribution d’une fausse passerelle et DNS  
5. Interception du trafic (MITM)

---

## 🔍 Détection

### ✔️ Méthode manuelle
- `ipconfig /all` → identifier le serveur DHCP
- `arp -a` → récupérer l’adresse MAC

### ✔️ Outil
- DHCPLOC → détecte les serveurs DHCP non autorisés

---

##  Prévention

- DHCP Snooping (switch)
- Segmentation réseau
- Surveillance (SIEM / IDS)
- Contrôle des équipements réseau

---

##  Compétences

- Réseaux (DHCP, TCP/IP)
- Cybersécurité (MITM, spoofing)
- Analyse réseau
- Détection d’intrusion

---

##  Conclusion

Ce projet montre comment une attaque DHCP peut compromettre un réseau et souligne l’importance de la **surveillance et sécurisation des infrastructures**.
