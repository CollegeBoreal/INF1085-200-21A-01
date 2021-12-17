## 300121460

## :whale: Mon projet sur MediaWiki!

## 🍎: Création d'une page MediaWiki avec UBUNTU 20.04. LTS

🏁: Dans ce tutoriel, nous allons procéder étape après étape à la création d'une page MediaWiki. 🌹 MediaWiki est un moteur de wiki pour le Web. Il est utilisé par l’ensemble des projets de la Wikimedia Foundation, des wikis hébergés chez FANDOM, ainsi que par de nombreux autres wikis (Utilisateur de Wiki). 🏁

## Table des matières:
1: Mise à jour de notre système

2: Mise en place de LAMP serveur

3: Installation et configuration manuelle de Apache web serveur

4: Installation d'une Base de Données SQL

5: Installation de PHP

6: Installation et Configuration de MediaWiki

7: Installation et Configuration de Apache web serveur sur CentOS

## Etape 1: Mise à jour de notre système

☑️: Commande permettant de mettre à jour notre système

```
sudo apt update
```
![Capture d’écran (553)](https://user-images.githubusercontent.com/71027883/146571308-5c6ebaa5-3cab-42e9-8ce2-600ffdf9efaf.png)

```
sudo apt upgrade
```
![Capture d’écran (603)](https://user-images.githubusercontent.com/71027883/146572625-68fd6623-9cb6-4e46-8c07-6e3e2e87a855.png)

## Etape 2: Mise en place de LAMP serveur

☑️: Commande permettant de mettre en place de LAMP serveur

☑️: LAMP est un acronyme pour Linux, Apache, MySQL, PHP. C'est une pile logicielle comprenant le système d'exploitation, un serveur HTTP, un système de gestion de bases de données et un langage de programmation interprété, et qui permet de mettre en place un serveur web.
[Linux] : le système d'exploitation, on peut déployer la pile LAMP sur la plupart des distributions GNU/Linux ;
[Apache] :  le serveur HTTP, il permet au serveur de communiquer avec le navigateur en utilisant le protocole HTTP(S) ;
[MySQL or Mariadb] : il s'agit d'un serveur de bases de données. Il sert à stocker, à manipuler et à accéder à des listes de données organisées en tableaux. Ce service peut être fournit par le logiciel MySQL ou par MariaDB (fork plus ouvert, plus performant, et 100% compatible MySQL).
[Perl, Perl or Python] :  PHP est un langage de programmation interprété qui permet de générer du contenu web dynamiquement. Il s'agit la plupart du temps de pages HTML).
☑️: Pour en savoir plus, référez-vous au lien suivant: ✔:(https://doc.ubuntu-fr.org/lamp)


```
sudo apt install lamp-server^
```
![Capture d’écran (544)](https://user-images.githubusercontent.com/71027883/146573628-6fb7224d-a7b0-4669-9ce6-4f74dd2e9382.png)

## Etape 3: Configuration manuelle de Apache web serveur

☑️: On doit commencer par installer Apache serveur sur notre serveur en utilisant la commande:

```
sudo apt install apache2
```

☑️: Après avoir installé Apache, et que ça fonctionne, vous pouvez l'adresse IP de votre serveur ou l'adresse URL pour voir la page par défaut de votre serveur Apache, ici c'est mon adresse IP 10.13.237.32 qui me permet d'avoir une idée sur la connexion à mon serveur Apache:

![Capture d’écran (604)](https://user-images.githubusercontent.com/71027883/146575782-953fd215-af68-4c6f-b934-5c636b9d803d.png)

## Etape 4: Installation d'une Base de Données SQL

☑️: On doit commencer par installer Apache serveur sur notre serveur en utilisant la commande:

```
sudo apt install apache2
```




## 🐳: References 🐳: :

✔️ :(https://www.manning.com/books/linux-in-action)

✔️ :(https://www.cyberithub.com/how-to-install-setup-mediawiki-on-ubuntu-20-04-lts-easy-steps/#Step_7_Install_MediaWiki)

✔️ :(https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units-fr)

✔️ :(https://www.reddit.com/r/mediawiki/comments/kyvbzb/mediawiki_135_internal_error_installing_some_php/)






## 🍎: Merci pour votre visite! 🍎: : 
