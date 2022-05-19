## 1.DESCRIPTION (SAMBA) :

Samba est un logiciel d'interopérabilité qui implémente le protocole propriétaire SMB/CIFS de Microsoft Windows dans les ordinateurs tournant sous le système d'exploitation Unix et ses dérivés de manière à partager des imprimantes et des fichiers dans un réseau informatique. 

## 2.INSTALLATION DU SAMBA:

$ sudo apt install samba

## 3.Ajouter les comptes utilisateurs à la base de données Samba :

Après avoir installé le serveur Samba 


L’administration des comptes utilisateurs est contrôlée par la commande smbpasswd comprenant quatre paramètres a, x, d et e représentés par leurs lignes de commandes respectives comme ci-dessous :

$ sudo smbpasswd -a NOM UTILISATEUR (MOT DE PASSE)

$ sudo smbpasswd -x NOM UTILISATEUR

$ sudo smbpasswd -d NOM UTILISATEUR

$ sudo smbpasswd -e NOMU TILISATEUR 

#### Le serveur peut charger et prendre en compte toutes les modifications effectuées grâce à la commande suivante :

$ sudo service smbd reload 

## 4.CONFIGURATION ET AUTORISATION 

Si vous souhaitez par exemple partager un dossier avec des photos et autorisant des ajouts et modifications d’autres utilisateurs, vous pouvez configurer ces paramètres avec les commandes suivantes :

[Photos]

path= /documents/photos

writeable = yes

guest ok = yes

#### Pour l'autorisation, il suffit de taper la commande:

$ chmod 777 [le nom de dossier] 

### Et Maintenant vous avez réussi à installer Samba 👍





