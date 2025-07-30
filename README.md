# D-ploiement-de-WordPress-sur-AWS-EC2

Ce projet illustre le déploiement automatisé d’un site WordPress sur une instance **AWS EC2** via un script Bash.  
Il comprend la création de l’instance, l’installation des dépendances nécessaires, la configuration d’Apache et MySQL, puis le déploiement de WordPress.

---

##  Objectifs du projet

- Créer une instance **EC2** (Ubuntu).
- Ouvrir les ports nécessaires (22, 80, 443).
- Installer et configurer **Apache, PHP et MySQL**.
- Déployer et configurer WordPress automatiquement via un script.

---

##  Prérequis

- Un compte **AWS** actif.
- Une paire de clés SSH pour accéder à l'instance EC2.
- **Git** et un terminal (bash ou PowerShell).

---

##  Déploiement

# 1. Lancer l’instance EC2
1. Connectez-vous à AWS Console et créez une instance **Ubuntu t2.micro**.
2. Configurez le groupe de sécurité pour ouvrir les ports :
   - 22 (SSH)
   - 80 (HTTP)
   - 443 (HTTPS)

# 2. Connexion SSH

ssh -i "votre-cle.pem" ubuntu@<IP_PUBLIQUE>

# 3. Transférer le script et l'exécuter

scp -i "votre-cle.pem" scripts/ScriptWordPress2.sh ubuntu@<IP_PUBLIQUE>:/home/ubuntu/
ssh -i "votre-cle.pem" ubuntu@<IP_PUBLIQUE>
chmod +x ScriptWordPress2.sh
./ScriptWordPress2.sh

 # Résultat

Une fois le script exécuté, accédez à WordPress via votre navigateur :
http://<IP_PUBLIQUE_EC2>

📜 Licence
Ce projet est libre d'utilisation à des fins éducatives.
