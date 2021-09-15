
# Blog


Creer un blog (i.e. Wordpress) permettant de décrire l'installation de:

* Linux [Ubuntu 20.04LTS](https://releases.ubuntu.com/20.04/) plus précisément installer la version  Serveur en [64-bit](https://releases.ubuntu.com/20.04/ubuntu-20.04.1-live-server-amd64.iso)

## Creer un blog (i.e. wordpress.com)

Le `blog` permettra de décrire toute la recherche effectuée pour installer Linux sur les machines [HP Proliant G6 ou G7](https://github.com/CollegeBoreal/Laboratoires/tree/master/3202/proliant)

Astuces: 

* Utiliser un CD-Rom (si vous en avez un) ou une clé USB pour `booter` sur la machine

* Installer la machine dans le laboratoire:

       Choisir une adresse dans la plage de réseau:
       
       - Externe: 10.13.237.0/24
       
       
## Legende

| :hash:             | Commentaires                                  |
|--------------------|-----------------------------------------------|
| :zero:             | Aucune installation, ne peut pas être véfifié |
| :one:              | Blog Créé                                     |
| :two:              | Blog et Réseau Externe créé                   |
| :heavy_check_mark: | Prêt à être noté                              |

## Liste des blogs

|:hash:| :id:      |   Blog (https://wordpress.com)                                                    | [VPN](https://github.com/CollegeBoreal/Tutoriels/tree/master/V.VPN)  | [Check](README.md#legende) | [Reseau Externe](README.md#one-reseau-externe)|
|------|-----------|-----------------------------------------------------------------------------------|------|--------------------|---------------|
| 01   | 300106677 | https://linux171117329.wordpress.com                                              | :x:  | :x:                | 10.13.237.?   |
| 02   | 300117811 |                                                                                   | :x:  | :x:                | 10.13.237.?   |
| 03   | 300121460 |                                                                                   | :x:  | :x:                | 10.13.237.?   |
| 04   | 300122014 |                                                                                   | :x:  | :x:                | 10.13.237.?   |


#### Example
| :id:      |   Blog (https://wordpress.com)                          |
|-----------|---------------------------------------------------------|
| 300098957 | https://setrar.wordpress.com/2015/01/10/bitstamp/       | 


## References

### :one: Reseau Externe

http://jodies.de/ipcalc?host=10.13.237.0&mask1=25

       Address:   10.13.237.0           00001010.00001101.11101101.0 0000000
       Netmask:   255.255.255.128 = 25  11111111.11111111.11111111.1 0000000
       Wildcard:  0.0.0.127             00000000.00000000.00000000.0 1111111
       =>
       Network:   10.13.237.0/25        00001010.00001101.11101101.0 0000000 (Class A)
       Broadcast: 10.13.237.127         00001010.00001101.11101101.0 1111111
       HostMin:   10.13.237.1           00001010.00001101.11101101.0 0000001
       HostMax:   10.13.237.126         00001010.00001101.11101101.0 1111110
       Hosts/Net: 126                   (Private Internet)

### :x: Reseau Interne

http://jodies.de/ipcalc?host=10.13.0.0&mask1=20

       Address:   10.13.0.1             00001010.00001101.0000 0000.00000001
       Netmask:   255.255.240.0 = 20    11111111.11111111.1111 0000.00000000
       Wildcard:  0.0.15.255            00000000.00000000.0000 1111.11111111
       =>
       Network:   10.13.0.0/20          00001010.00001101.0000 0000.00000000 (Class A)
       Broadcast: 10.13.15.255          00001010.00001101.0000 1111.11111111
       HostMin:   10.13.0.1             00001010.00001101.0000 0000.00000001
       HostMax:   10.13.15.254          00001010.00001101.0000 1111.11111110
       Hosts/Net: 4094                  (Private Internet)
