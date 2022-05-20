## 1.DESCRIPTION (APACHE) 

Le serveur Web Apache est un serveur HTTP open source pour les systèmes d'exploitation modernes, notamment Linux et Windows.
C'est le serveur Web le plus populaire sur Internet. Le fichier de configuration d'Apache et la méthode d'installation varient selon les différentes distributions de Linux.
Mais la racine du document par défaut est /var/www/htmldans toutes les distributions.

## 2.INSTALLATION 

$ apt-get install apache2

#### * Exécutez la commande suivante pour démarrer le processus Apache:

$ /etc/init.d/apache2 start

## 3.CONFIGURATION 

Le répertoire de configuration d'Apache est:

$ /etc/apache2 et
$ apache2.conf

#### *Créez un fichier à 

¢ /etc/apache2/sites-available/yourdomain.com.

#### *ajoutez-y les lignes suivantes :

$ nano /etc/apache2/sites-available/yourdomain.com.conf 

<virtualhost *:80="">  

ServerAdmin webmaster@localhost  

ServerName yourdomain.com  

ServerAlias www.yourdomain.com  

DocumentRoot /var/www/yourdomain.com  

ErrorLog ${APACHE_LOG_DIR}/error.log  

CustomLog ${APACHE_LOG_DIR}/access.log combined  

</virtualhost>
