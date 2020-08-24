# howto-pi
Tutoriel de base pour les gros NOOBS ! :)

# Prérequis
* 1x Raspberry Pi 2/3/4 ou Raspberry Pi Zero
* 1x Carte micro-SD 8GB (16GB recommandé)

# Télécharger Raspberry Pi OS
Pour télécharger Raspberry Pi OS, il suffit de se rendre sur le site de la fondation Raspberry Pi.
https://www.raspberrypi.org/downloads/

Préferer la version *lite* (plus légère en ressources et en mémoire) à la version *desktop*

Pour une installation de dev, il est possible d'utiliser NOOBS.
https://www.raspberrypi.org/downloads/noobs/

**Attention, NOOBS n'est pas recommandé dans un environnement de prod. Il ralentit le démarrage du raspberry !**

# Préparer la carte SD
Pour copier sur la carte SD l'image téléchargée précédemment, il faut utiliser le logiciel prévu a cet effet Raspberry Pi Imager.
https://www.raspberrypi.org/downloads/

# Préparer Raspberry Pi OS
Avant de démarrer le raspberry, il convient de faire quelques préréglages.
1. Insérer la carte SD dans l'ordinateur.
2. Créer un fichier nommé ssh (sans extension) à la racine de la carte SD. //Doit correspondre à /boot
3. Créer un fichier nommé wpa_supplicant.conf à la racine de la carte SD. //Doit correspondre à /boot
4. Dans le fichier mettre ceci:
```
country=CH
network= {
ssid="NOM_DE_MON_SSID"
psk="MON_MOT_DE_PASSE"   
}
```

Le raspberry est maintenant prêt a démarrer, se connecter au réseau WIFI et être accessible par ssh via le réseau Ethernet.

# 1er démarrage du Raspberry Pi
Lors du premier démarrage du raspberry, il convient de faire quelques réglages.

Tout d'abord se connecter au raspberry avec ssh, une fois connecté effectuer les commandes suivantes dans le terminal.

1. Mettre à jour la liste des paquets:

    * `sudo apt-get update`

2. Mettre à jour le système:

    * `sudo apt-get upgrade -y`

3. Faire une mise à niveau:

    * `sudo apt-get dist-upgrade -y`

4. Eteindre le raspberry:

    * `sudo shutdown 00`

# DEV
NOM | MAIL
----|----
PIANZOLA Cédric | pianzola.cedric@p-tc.ch
