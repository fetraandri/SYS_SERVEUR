# 1.DESCRIPTION (NGINX) :

Nginx (Engine X, prononcez "n-gèn-x") est un serveur Web asynchrone écrit par Igor Sysoev pour les besoins d'un site russe à très fort trafic.
Il peut être configuré pour faire office de serveur reverse proxy Web et de serveur proxy de messagerie électronique (IMAP/POP3).

# 2.INSTALLATION 

$ sudo apt-get install nginx

Vous pouvez le vérifier avec la commande:

$ sudo nginx -v  

Vous avez maintenant nginx installé sur votre serveur mais pas prêt à servir des pages Web.
vous devez démarrer le nginx. Vous pouvez le faire en utilisant cette commande :

$ sudo systemctl start nginx 

# 3.REGLAGE PAR FEUX 

Avant de tester Nginx, vous devez régler votre logiciel de pare-feu pour autoriser l’accès au service. Lors de l’installation, Nginx s’enregistre en tant que service avec ufw afin d’en faciliter l’accès.

Énumérez les configurations d’application avec lesquelles ufw sait travailler en saisissant :

$ sudo ufw app list

### Vous devriez obtenir une liste des profils de l’application,vous pouvez l’activer en tapant :

$ sudo ufw allow 'Nginx HTTP'

# 4.CONFIGURATION DU SERVEUR

#### ./etc/nginx : répertoire de configuration Nginx. Tous les fichiers de configuration Nginx se trouvent ici.

#### ./etc/nginx/nginx.conf : fichier de configuration principal de Nginx.
Celui-ci peut être modifié pour apporter des changements à la configuration globale de Nginx.

#### ./etc/nginx/sites-available/: répertoire dans lequel vous pouvez stocker les blocs de serveur par site.
Nginx n’utilisera pas les fichiers de configuration trouvés dans ce répertoire à moins qu’ils ne soient liés au répertoire sites-enabled.
En règle générale, la configuration de tous les blocs de serveur se fait dans ce répertoire, puis s’active en établissant une liaison avec l’autre répertoire.

#### ./etc/nginx/sites-enabled/: répertoire dans lequel les blocs de serveur par site activés sont stockés.
En règle générale, ils sont créés en reliant les fichiers de configuration trouvés dans le répertoire sites-available.

#### ./etc/nginx/snippets: ce répertoire contient des fragments de configuration qui peuvent être inclus ailleurs dans la configuration Nginx. Les segments de configuration potentiellement reproductibles sont de bons candidats pour la refactorisation en fragments.

### Et maintenant votre serveur Web est installé . Bonne chance!








