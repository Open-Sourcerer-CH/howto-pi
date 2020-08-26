# Tuto pour bien débuter avec un *Raspberry Pi* !
<p align="center">
  <img width="200" height="200" src="/img/raspberrypi-400x400.png">
</p>
<p align="center">
  <img width="200" height="200" src="/img/RASPBERRY PI - V3 - 400x400.jpg">
</p>

:checkered_flag: Tutoriel de base pour les gros *NOOBS* ! :checkered_flag:

On démarre de zéro pour que ce tutoriel soit accessible au plus grand nombre. Tu veras ca va être :thumbsup:

Dans peu de temps tu seras toi aussi un ***apprenti sorcier*** et tu pourras porter ce titre fierement grâce au ***catalyseur*** que tu te seras fabriqué.

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

De bonnes bases en informatiques sont nécéssaire et un ordinateur en état de marche avec au choix *Windows/Mac/Linux*.

Des connaissances de *Linux* sont recommandés mais pas indispensables. Toutefois il est obligatoire de savoir utiliser des *lignes de commandes* dans un *terminal* et savoir se connecter à un serveur en *ssh*.

Tu ne connais pas encore le *ssh* ?

Alors ce tuto est fait pour toi [Tuto | Se connecter à un *Raspberry Pi* à l'aide de *ssh*]() !

Afin d'être compris par un maximum de personnes, nous décrirons au mieux chacune des commandes que nous utiliserons.

Tu n'as pas de *Raspberry Pi* et tu souhaites en acheter un ?

Nous te proposons plusieurs possibilités,
1. Sur le site officiel de la *Raspberry Pi Foundation* en cliquant [ici](https://www.raspberrypi.org/) .
2. Sur le site de vente en ligne *Adafruit* en cliquant [ici](https://www.adafruit.com/) .
3. Sur le site de vente en ligne (suisse) *Galaxus* en cliquant [ici](https://www.galaxus.ch) .
4. Sur le site de vente en ligne (suisse) *Pi-Shop* en cliquant [ici](https://www.pi-shop.ch) .

Si tu remplis toutes les conditions, alors tu peux passer à l'étape suivante. Amuses toi bien.

# Télécharger Raspberry Pi OS
Pour télécharger *Raspberry Pi OS*, il te suffit de te rendre sur le site de la *Raspberry Pi Foundation* à la section *Downloads* .
https://www.raspberrypi.org/downloads/

Si tu débutes avec le *Raspberry Pi* et que c'est ta première utilisation alors il est recommandé d'utiliser la version *full*. Cette version contient l'OS ainsi qu'une selection de logiciels recommandés. Le choix idéal pour découvrir les possibilités offertes par ce petit bijoux. :gem:

Pour des projets de type *IoT* il est préférable d'utiliser la version *lite* plus légère en ressources et en mémoire que les versions *desktop* et *full*.

Pour une installation de developpement, il est possible d'utiliser *NOOBS* l'utilitaire créé par la *Raspberry Pi Foundation*.
https://www.raspberrypi.org/downloads/noobs/

**Attention, ne pas utiliser *NOOBS* dans un environnement de prod. Il ralentit le démarrage du raspberry !**

# Préparer la carte SD
Pour copier sur la carte SD l'image téléchargée précédemment, il faut utiliser le logiciel prévu a cet effet *Raspberry Pi Imager*.
https://www.raspberrypi.org/downloads/

# Préparer Raspberry Pi OS
Avant de démarrer le raspberry, il convient de faire quelques préréglages.
1. Insérer la carte micro-SD dans l'ordinateur.
2. Créer un fichier nommé ssh (sans extension) à la racine de la carte SD.
3. Créer un fichier nommé wpa_supplicant.conf à la racine de la carte SD.
4. Dans le fichier mettre ceci: (Pour la suisse)
```
country=CH
network= {
ssid="NOM_DE_MON_SSID"
psk="MON_MOT_DE_PASSE"   
}
```
Tu l'auras certainement compris, il faut remplacer "NOM_DE_MON_SSID" par le nom du réseau WIFI auquel tu souhaites te connecter et remplacer "MON_MOT_DE_PASSE" par le mot de passe du réseau WIFI. C'est aussi simple que ca !

Le *Raspberry Pi* est maintenant prêt a démarrer, se connecter au réseau WIFI et être accessible par *ssh* via le réseau.

# 1er démarrage du Raspberry Pi
Lors du premier démarrage du raspberry, il convient de faire quelques réglages.

Nous allons vois la procédure pour un *Raspberry Pi* installer sans écran ni clavier ni souris. Ce type d'installation est appelé *Headless* c'est-à-dire *sans tête*.

Brancher le *Raspberry Pi* sur le secteur au moyen de l'adaptateur fourni.

Patientes une bonne petite minute pour laisser le temps au *Raspberry Pi* de démarrer correctement et d'initialiser les processus.

Ensuite, connectes toi au *Raspberry Pi* avec *ssh*. 

Une fois connecté effectues les commandes suivantes dans le terminal.

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
Voilà ! Ton ***catalyseur*** est prêt ! Avec un ***grimoire magique*** ton équipement d'***apprenti sorcier*** sera au complet !

Mais pas de hâte nous verrons cela dans notre prochain tutoriel.

Tu disposes maintenant d'un *Raspberry Pi* tout frais tout neuf ! Un vrai petit geek ! :neckbeard:

:checkered_flag: Tu es fin prêt pour entré dans le vif de l'action ! :checkered_flag:


Maintenant il ne te reste plus qu'a choisir un projet de rêve parmi la liste ci-dessous :
NOM | DESCRIPTION | URL
----|-------------|-----
MagicMirror2 | Un mirroir magique | [howto-pi-magicmirror2]()
LED APA102 | Piloter des LEDs RGBWW (APA102) | [howto-pi-led-apa102]()

# SUPPORT
Tu as besoin d'aide pour la réalisation de ton projet ?

:question: Poses ta question sur notre [forum](https://www.opensourcerer.ch/forums) d'entraide ! :question:

# DEV
Rédiger avec :heart: par ***PIANZOLA Cédric*** pour la communauté [*Open Sourcerer [CH]*](https://www.opensourcerer.ch) !

NOM | MAIL | SITE
----|------|------
PIANZOLA Cédric | pianzola.cedric@p-tc.ch | www.p-tc.ch

:bulb: N'hésites pas à me faire part de tes remarques et commentaires. :bulb:

Toutes les critiques sont les bienvenues.

:exclamation: Restes informé de nos dernières inventions en t'abonnant à notre flux [*RSS*](https://www.opensourcerer.ch/feed) ! :exclamation:
