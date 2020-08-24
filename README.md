# Comment bien démarrer avec un *Raspberry Pi* !
Tutoriel de base pour les gros *NOOBS* ! :)

# Prérequis
* 1x Raspberry Pi 2/3/4 ou Raspberry Pi Zero
* 1x Carte micro-SD 8GB (16GB recommandé)

# Télécharger Raspberry Pi OS
Pour télécharger *Raspberry Pi OS*, il suffit de se rendre sur le site de la *Raspberry Pi Foundation*.
https://www.raspberrypi.org/downloads/

Si vous débutez avec le *Raspberry Pi* il est recommandé d'utiliser la version *full*. Cette version contient l'OS ainsi qu'une selection de logiciels recommandés.

Pour des projets de type IoT préferez la version *lite* (plus légère en ressources et en mémoire) à la version *desktop* ou *full*.

Pour une installation de dev, il est possible d'utiliser *NOOBS* l'utilitaire créé par la *Raspberry Pi Foundation*.
https://www.raspberrypi.org/downloads/noobs/

**Attention, *NOOBS* n'est pas recommandé dans un environnement de prod. Il ralentit le démarrage du raspberry !**

# Préparer la carte SD
Pour copier sur la carte SD l'image téléchargée précédemment, il faut utiliser le logiciel prévu a cet effet *Raspberry Pi Imager*.
https://www.raspberrypi.org/downloads/

# Préparer Raspberry Pi OS
Avant de démarrer le raspberry, il convient de faire quelques préréglages.
1. Insérer la carte SD dans l'ordinateur.
2. Créer un fichier nommé ssh (sans extension) à la racine de la carte SD. (Doit correspondre à /boot)
3. Créer un fichier nommé wpa_supplicant.conf à la racine de la carte SD. (Doit correspondre à /boot)
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

1. Lancer l'assistant de configuration dédié du raspberry :
    1. `sudo raspi-config`
2. Procéder à la configuration souhaitée principalement,
    1. Paramètres régionaux
    2. Paramètres réseaux
3. Changer le mot de passe de l'utilisateur pi: 
    1. `passwd`
    2. Taper le nouveau mot de passe
4. Mettre à jour la liste des paquets:
    1. `sudo apt-get update`
5. Mettre à jour le système:
    1. `sudo apt-get upgrade -y`
6. Faire une mise à niveau:
    1. `sudo apt-get dist-upgrade -y`
7. Redémarrer le raspberry:
    1. `sudo reboot 00`
8. Vérifier que tout se passe bien.
9. Eteindre le raspberry:
    1. `sudo shutdown 00`

# DEV
NOM | MAIL | SITE
----|------|------
PIANZOLA Cédric | pianzola.cedric@p-tc.ch | www.p-tc.ch
