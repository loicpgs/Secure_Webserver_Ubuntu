# 🔐 Secure Webserver on Ubuntu (Nginx + HTTPS)

Déploiement d’un serveur web sécurisé via HTTPS auto-signé dans une VM Ubuntu Server, gérée avec Vagrant. Projet orienté TSSR : configuration de service, sécurité réseau et automatisation.

---

## 📦 Fonctionnalités

- 💻 Déploiement automatique d'une VM Ubuntu 20.04 (Vagrant + VirtualBox)
- 🌐 Serveur web Nginx installé et configuré
- 🔒 HTTPS activé avec certificat auto-signé
- 🔁 Redirection HTTP vers HTTPS
- 🧾 Page web personnalisée (HTML)
- 🛡️ Pare-feu configuré avec UFW (ouvert uniquement : 22, 80, 443)

---

## 🚀 Lancer le projet

**1. Cloner ce dépôt :**
  
   git clone https://github.com/<ton-utilisateur>/secure-webserver-ubuntu.git
   cd secure-webserver-ubuntu

**2. Démarrer la VM :**

vagrant up

**3. Accéder au serveur :**

http://192.168.56.10 → redirection vers HTTPS

https://192.168.56.10 (certificat auto-signé, acceptez l’avertissement)

**4. Se connecter en SSH :**

vagrant ssh

# 🧾 Configuration utilisée :

**OS :** Ubuntu Server 20.04 (focal64)

**Webserver :** Nginx 1.18

**HTTPS :** certificat auto-signé (OpenSSL)

**Pare-feu :** UFW (ports ouverts : 22, 80, 443)

**Réseau :** IP privée 192.168.56.10

# 📁 Arborescence :

secure-webserver-ubuntu/
├── Vagrantfile
├── setup/
│   └── index.html
├── README.md
├── notes.md  (optionnel : journal, commandes, erreurs)
└── .gitignore

 # 🔧 Évolutions possibles

**Ajouter un script d’installation** (setup.sh)

**Utiliser DuckDNS** ou **No-IP** pour tester Let’s Encrypt

*Ajouter des **en-têtes HTTP de sécurité** (HSTS, CSP…)

*Intégrer une **supervision simple** (Zabbix agent, etc.)


# Licence :

MIT
