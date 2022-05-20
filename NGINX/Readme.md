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
