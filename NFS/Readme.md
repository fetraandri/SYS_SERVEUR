# 1.DESCRIPTION (NFS) 

Ce système de fichiers en réseau permet de partager des données principalement entre systèmes de type UNIX mais des versions existent également pour Microsoft Windows™ et Mac.

# 2.INSTALLATION 

Ici, on va détailler l'installation d'un serveur NFS et montrer comment connecter un client à ce partage.

#### *L'installation :

$ apt install nfs-kernel-server

# 3.CONFIGURATION 

### & Partie Client:

Pour la paverrtie cliente, on installe les paquets adéquats :

$ apt install nfs-common
$ mkdir -p /media/nfs
mount -t nfs 192.168.21.200:/media/partage /media/nfs

Avec la commande df, on peut voir que tout est monté :

$ df -h
Filesystem            Size  Used Avail Use% Mounted on
192.168.21.200:/media/partage       20G  985M   18G   5% /media/nfs
