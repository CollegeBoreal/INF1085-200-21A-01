# 300122014

## :roll_of_paper: vpn

## 🐳:CONNECTION VPN SUR UBUNTU 20.04. LTS

🏁: Dans ce tutoriel, vous aller apprendre de la maniere la plus simple comment creer un OPEN VPN sur votre votre server Debian . 🌹 OpenVPN est un logiciel libre permettant de créer un réseau privé virtuel VPN il cree une sorte de tunnel qui va vous permettre de vous connecter a distance a votre server du College boreal 🏁

## Table des matières:
1.Mise à jour du systeme 
2.Trouver notre adresse IP
3.Telecharger et executer OpenVpn
4.copie du fichier openVpn sur la machine cliente
5:Installation d'OpenVpn sur notre Ordinateur portable(machine cliente) 

🥇:Nous devons créer un OPENVPN sur notre Serveur Linux

![01](https://user-images.githubusercontent.com/71392439/146131678-456fd459-9b61-44e5-9cbf-4f432aaa7033.png)


☑️:Nous allons creer un tunnel pour nous permettre de se connecter à distance à distance sur notre serveur du college .ce tunnel est une application VPN Open sourfce qui vas permettre d'atteindre notre reseau privé.Les etapes élaborer ci dessous nous permettrons de realiser un OpenVpn sur notre serveur

![02](https://user-images.githubusercontent.com/71392439/146132735-56bb10f4-7fd1-480f-b126-5596c456fe4b.png)

## Etape 1: Mise à jour de notre système 

☑️:commande permettant de mettre à jour notre système

```
sudo apt update
```
![Capture d’écran 2021-12-12 224106](https://user-images.githubusercontent.com/71392439/146133668-88ee57fe-82b9-4afc-8f15-0c21308b55f3.png)

```
sudo apt upgrade
```
![upgrade](https://user-images.githubusercontent.com/71392439/146133807-5817ef63-1c61-452a-b0dd-5bdd5fe6b6ad.png)

## Etape 2: Trouver notre adresse IP et la notée

☑️ À l'aide de la commande suivante
```
ip address
```
![ipaddress](https://user-images.githubusercontent.com/71392439/146134073-6af6208d-adcb-4ab4-a468-cb8d337520d3.png)

## Etape 3: Telecharger et executer OpenVpn

☑️:commande de telechargement du script

```
wget https://git.io/vpn -O openvpn-ubuntu-install.sh
```

![openvpn installer](https://user-images.githubusercontent.com/71392439/146134533-414a7d54-a74b-4223-89ba-be291a8e57f8.png)


☑️:Nous devoons rendre le script éxécutable après le téléchargement avec cette commande

```
chmod -v +x openvpn-ubuntu-install.sh
```
![script executable](https://user-images.githubusercontent.com/71392439/146134755-4ad5675f-d5ae-4a1e-b95a-373bb233b2bd.png)


☑️: une fois que la permission à été démandé a notre serveur pour executer le script on peut ouvrir notre script avec l'éditeur nano/vim

```
 nano openvpn-ubuntu-install.sh
```
![nano1](https://user-images.githubusercontent.com/71392439/146135406-56e03ff2-bef8-4c7e-b920-3ce86ada2f36.png)

![nano](https://user-images.githubusercontent.com/71392439/146135188-4fb6ade1-973b-4425-9005-8d8f71167cb8.png)

☑️:Nous exécutons notre script avec la commande suivante:

```
sudo ./openvpn-ubuntu-install.sh
```
![Capture d’écran 2021-12-12 153054](https://user-images.githubusercontent.com/71392439/146136610-2b02f1eb-a7fd-4ebd-9071-54a09bb39b57.png)

![adresseip](https://user-images.githubusercontent.com/71392439/146137114-73fbe810-d245-4165-9de7-59c36cd9e529.png)




 ☑️:Vous devez repondre a une serie de question avant l'installation de l'openVpn
 🔖:  On remarque ici que le système nous a donné notre adresse IP publique qu’il a convertir grâce à notre adresse IP privée. Notre adresse IP publique ici est 205.211.23.237
 🔖: Choisir le procole que  l'OpenVPN doit utiliser. Dans notre cas nous avons choisir le protocole UDP qui est d’ailleurs recommande par le système
🔖:l'openVpn vas Utiliser le port 1194
🔖:nous choisissons un DNS par defaut qui est 1.1.1.1
🔖:Enfin nous mettons le nom de notre client. Nous avons la possibilité d'ajouter autant de client possible


☑️:Nous avons les commandes nous permettant d'arreter, demarrer , redemarrer et voir le statut de notre OpenVptn grace aux commandes suivantes:
```
 sudo systemctl stop openvpn-server@server.service
 sudo systemctl start openvpn-server@server.service
 sudo systemctl restart openvpn-server@server.service
 sudo systemctl statut openvpn-server@server.service
```
☑️:Dans notre cas nous allons verifier le statut de L'openVpn

```
 sudo systemctl status openvpn-server@server.service
```
![final](https://user-images.githubusercontent.com/71392439/146138657-d6c8146e-3f96-456a-9a0b-b297e2cc38c0.png)
![clientsylvain](https://user-images.githubusercontent.com/71392439/146138811-b04fb045-9007-43d7-9b6b-499166f7d5c0.png)

☑️:si nous faisons la commande IP address nous remarquerons que notre OpenVpn a été bien créer"Nous verrons donc le tunnel Point par point avec l'adresse IP qui nous été attribuée

![03](https://user-images.githubusercontent.com/71392439/146139823-79e4506d-721c-4836-84c1-c0ed462ef5b8.png)

## Etape 4:Copier notre fichier OpenVpn sur notre ordinateur portbale considéré comme machine cliente

```
$ ssh sylvainmakak@10.13.237.28 "sudo -S cat /root/sylvain.ovpn" > sylvain.ovpn
```
![sylvain](https://user-images.githubusercontent.com/71392439/146140554-d5c37a50-758f-4309-b804-6966af092d88.png)

☑️:faire la commande ls pour voir oû est localiser notre fichier OpenVpn dans notre ordinateur

![lscomande](https://user-images.githubusercontent.com/71392439/146140714-e94c788c-362d-4dd5-9b4c-b8ae9e4f95e7.png)
## Etape 5: Installation d'OpenVpn sur notre Ordinateur portable(machine cliente) 

☑️:vous pouvez utiliser le shell pour l'installer avec la commande suivante:
```
 Choco install openvpn
```
![choco](https://user-images.githubusercontent.com/71392439/146141553-033383ff-5bc5-4e93-b4c7-429486d3f9f9.png)


☑️:vous pouvez aussi le telecharger le l'executer sur votre ordinateur via le lien ci-dessous

```
https://openvpn.net/client-connect-vpn-for-windows/
```

☑️:Trouvez l'emplacment du fichier installer dans l'ordinateur. Ouvrir le fichier et changer l'adressse IP publique par votre adresse Ip privée
![emplacement](https://user-images.githubusercontent.com/71392439/146142169-207875c4-2773-45d6-9619-bc2f6c5e96fa.png)
![Add1](https://user-images.githubusercontent.com/71392439/146142740-b532a5c4-122e-4269-8ac9-abbfc0f8e8a7.png)
![05](https://user-images.githubusercontent.com/71392439/146152121-cfd1679f-f7ab-4088-b4e1-571bbcdb19fc.png)


☑️:Enregistrer le fichier puis changer l'emplacement
```
program files, openvpn, config
```
![Capture d’écran 2021-12-12 233039](https://user-images.githubusercontent.com/71392439/146143043-0103e623-1bf4-4aaa-9d47-1f20e594457e.png)


☑️:Faire un clic droit sur l’icône OpenVPN GUI et allez a:
```
propriété, comptabilité et cocher rexecuter ce programme en tant qu'administrateur.
```
![Capture d’écran 2021-12-12 233401](https://user-images.githubusercontent.com/71392439/146143301-dcafa7c6-008f-4515-91a4-2b87da4a3656.png)
![Capture d’écran 2021-12-12 233504](https://user-images.githubusercontent.com/71392439/146143351-a75a8829-e08e-49ae-892f-45ba49f34930.png)


☑️:Une fois cela fais vous pouvez ouvrir OpenVPN dans votre ordinateur en doublecliquant sur l’icone qui est sur votre desktop ou en ouvrant le fichier a partir de la barre de tache dans le menu demarrer.

![4](https://user-images.githubusercontent.com/71392439/146144038-281265f8-1465-4cd3-bb2e-c140c2eb6782.png)
![5](https://user-images.githubusercontent.com/71392439/146144187-738e7b7e-0479-4fad-a2aa-a31626351703.png)

☑️:une fois que cela est fait vous pouvez ouvrir OpenVPN dans votre ordinateur en doublecliquant sur l’icone qui est sur votre desktop et en ouvrant le fichier a partir de la barre de tache dans le menu demarrer
![00](https://user-images.githubusercontent.com/71392439/146163007-0ab79dab-c68c-4978-a9b7-43814916bf91.png)

![06](https://user-images.githubusercontent.com/71392439/146175608-0b0d5746-cde2-4b0a-b272-79033b56f8eb.png)


☑️:Une fois connecté a notre VPN nous pouvons vérifier notre connexion avec le CMD Prompt. En faisant la commande IPconfig. Alors nous voyons apparaitre l’adresse IP de notre application OpenVPN qui est 10.8.0.2/24 et on remarque également en faisant la commande tracert 10.8.0.1 on vois le nombre de temps effectuer pour arriver a notre serveur. Aussi en faisant la commande IP a dans notre server on vois clairement nos deux adresses c’est-à-dire l’adresse IP de notre serveur et l’adresse IP openvpn

![07](https://user-images.githubusercontent.com/71392439/146164150-412128a2-1b76-4a63-8f41-d4792ed6ebf4.png)
![09](https://user-images.githubusercontent.com/71392439/146164312-86a02634-1d86-417c-ba20-7f422d8cadda.png)

☑️:  Pour ce connecter a notre OPENVPN vous devez vous servir de la cles que nous avons mis dans le key.txt de notre fichier.


   
## :sparkles: References :sparkles: :

:heavy_check_mark:(https://www.tecmint.com/install-openvpn-in-ubuntu/ )

:heavy_check_mark:(https://www.cyberciti.biz/faq/ubuntu-20-04-lts-set-up-openvpn-server-in-5-minutes/)


## ✨:Merci pour votre visite ✨



