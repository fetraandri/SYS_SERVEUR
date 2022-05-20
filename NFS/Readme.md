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



### Quelques options de montage utiles:

Au travail, j'utilise un partage NFS pour étendre du stockage pour un coût peu élevé.

Mais le système se comporte bizarrement lorsque le partage NFS est indisponible (reboot du NAS, perte temporaire de réseau).

Pour cela, on peut monter le partage NFS avec les options soft, retrans et timeo. Je choisis 2 retransmissions en cas d'échec et 5 dixièmes de secondes (500 ms) de timeout (le NAS et le serveur sont dans le même sous-réseau, sur le même switch):


$ mount -t nfs4 192.168.21.200:/media/partage /media/nfs -o soft,retrans=2,timeo=5

Ou dans /etc/fstab :

$ 192.168.21.200:/media/partage   /media/nfs   nfs      auto,_netdev,nofail,soft,retrans=2,timeo=5 0 0 

##### Et voilà, votre serveur est maintenant installé 👍
