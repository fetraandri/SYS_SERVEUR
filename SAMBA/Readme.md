## 1.DESCRIPTION (SAMBA) :

Samba est un logiciel d'interopérabilité qui implémente le protocole propriétaire SMB/CIFS de Microsoft Windows dans les ordinateurs tournant sous le système d'exploitation Unix et ses dérivés de manière à partager des imprimantes et des fichiers dans un réseau informatique. 

## 2.INSTALLATION DU SAMBA:

$ sudo apt install samba

## 3.CONFIGURATION DU SERVEUR:

Après avoir installé le serveur Samba 


L’administration des comptes utilisateurs est contrôlée par la commande smbpasswd comprenant quatre paramètres a, x, d et e représentés par leurs lignes de commandes respectives comme ci-dessous :

$ sudo smbpasswd -a NOM UTILISATEUR (MOT DE PASSE)

$ sudo smbpasswd -x NOM UTILISATEUR

$ sudo smbpasswd -d NOM UTILISATEUR

$ sudo smbpasswd -e NOMU TILISATEUR 






