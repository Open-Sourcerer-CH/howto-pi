# Comment bien démarrer avec un *Raspberry Pi* !
<p align="center">
  <img width="200" height="200" src="/img/raspberrypi-400x400.png">
</p>

:checkered_flag: Tutoriel de base pour les gros *NOOBS* ! :checkered_flag:

On démarre de zéro pour que ce tutoriel soit accessible au plus grand nombre. Tu veras ca va être :thumbsup:

Dans peu de temps tu seras toi aussi un apprenti sorcier et tu pourras porter ce titre fierement.

La marche à suivre décrite dans ce tuto est pour *Raspberry Pi OS* mais elle peut également s'appliquer pour tout un tas d'autres distributions *Linux* .
NOM | DESCRIPTION | SITE
----|-------------|------
LibreElec | Multimédia | https://www.libreelec.tv
OSMC | Multimédia | https://www.osmc.tv
Volumio | Audio HiFi | https://www.volumio.org

# Prérequis
* 1x *Raspberry Pi* 2/3/4 ou *Raspberry Pi* Zero
* 1x Carte *micro-SD* 8GB (16GB recommandé)
* 1x Adaptateur *micro-SD* vers *USB* ou *SD*

Tu n'as pas de *Raspberry Pi* et tu souhaites en acheter un ?

Nous te proposons plusieurs possibilités,
1. Sur le site officiel de la *Raspberry Pi Foundation* en cliquant [ici](https://www.raspberrypi.org/) .
2. Sur le site de vente en ligne *Galaxus* en cliquant [ici](https://www.galaxus.ch) .
3. Sur le site de vente en ligne *Pi-Shop* en cliquant [ici](https://www.pi-shop.ch) .

# Télécharger Raspberry Pi OS
Pour télécharger *Raspberry Pi OS*, il suffit de se rendre sur le site de la *Raspberry Pi Foundation* à la section *Downloads* .
https://www.raspberrypi.org/downloads/

Si tu débutes avec le *Raspberry Pi* il est recommandé d'utiliser la version *full*. Cette version contient l'OS ainsi qu'une selection de logiciels recommandés. Le choix idéal pour découvrir les possibilités offertes par ce petit bijoux. :gem:

Pour des projets de type *IoT* il est préférable d'utiliser la version *lite* (plus légère en ressources et en mémoire) aux versions *desktop* et *full*.

Pour une installation de dev, il est possible d'utiliser *NOOBS* l'utilitaire créé par la *Raspberry Pi Foundation*.
https://www.raspberrypi.org/downloads/noobs/

**Attention, ne pas utiliser *NOOBS* dans un environnement de prod. Il ralentit le démarrage du raspberry !**

# Préparer la carte SD
Pour copier sur la carte SD l'image téléchargée précédemment, il faut utiliser le logiciel prévu a cet effet *Raspberry Pi Imager*.
https://www.raspberrypi.org/downloads/

# Préparer Raspberry Pi OS
Avant de démarrer le raspberry, il convient de faire quelques préréglages.
1. Insérer la carte micro-SD dans l'ordinateur.
2. Créer un fichier nommé ssh (sans extension) à la racine de la carte SD. (Doit correspondre à /boot)
3. Créer un fichier nommé wpa_supplicant.conf à la racine de la carte SD. (Doit correspondre à /boot)
4. Dans le fichier mettre ceci: (Pour la suisse)
```
country=CH
network= {
ssid="NOM_DE_MON_SSID"
psk="MON_MOT_DE_PASSE"   
}
```
Le raspberry est maintenant prêt a démarrer, se connecter au réseau WIFI et être accessible par *ssh* via le réseau Ethernet.

# 1er démarrage du Raspberry Pi
Lors du premier démarrage du raspberry, il convient de faire quelques réglages.

Tout d'abord se connecter au raspberry avec *ssh*, une fois connecté effectuer les commandes suivantes dans le terminal.

1. Lancer l'assistant de configuration dédié du raspberry :
    1. `sudo raspi-config`
2. Procéder à la configuration souhaitée :
    1. Paramètres régionaux.
        * Région
        * Langue
        * Fuseau horraire
    2. Paramètres réseaux.
        * WIFI
    3. Paramètres avancé
        * Redimensionner la partition sur la carte *micro-SD*.
3. Changer le mot de passe de l'utilisateur pi :
    1. `passwd`
    2. Taper le nouveau mot de passe
4. Mettre à jour la liste des paquets :
    1. `sudo apt-get update`
5. Mettre à jour le système:
    1. `sudo apt-get upgrade -y`
6. Faire une mise à niveau:
    1. `sudo apt-get dist-upgrade -y`
7. Redémarrer le raspberry :
    1. `sudo reboot 00`
8. Vérifier que tout se passe bien.
9. Eteindre le raspberry :
    1. `sudo shutdown 00`

# PRET
Voilà !

Vous disposez maintenant d'un *Raspberry Pi* tout frais tout neuf ! Un vrai petit geek ! :neckbeard:

Maintenant il ne te reste plus qu'a choisir un projet de rêve parmi la liste ci-dessous :
NOM | DESCRIPTION | URL
----|-------------|-----
MagicMirror2 | Un mirroir magique | [howto-pi-magicmirror2]()

# SUPPORT
Tu as besoin d'aide pour la réalisation de ton projet ?

:question: Poses ta question sur notre [forum](https://www.opensourcerer.ch/forums) d'entraide !

Reste informé de nos dernières inventions en t'abonnant à notre flux [*RSS*](https://www.opensourcerer.ch/feed) !

# DEV

Rédiger avec :heart: par PIANZOLA Cédric pour la communauté ["Open Sourcerer [CH]"](https://www.opensourcerer.ch) !

NOM | MAIL | SITE
----|------|------
PIANZOLA Cédric | pianzola.cedric@p-tc.ch | www.p-tc.ch

N'hésites pas a me faire part de tes remarques et commentaires. :idea:

Toutes les critiques (constructives ...) sont les bienvenues.
