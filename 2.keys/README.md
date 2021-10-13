# 2 Keys

:one: Authoriser l'acces à sa machine au professeur

* Connectez vous à votre machine avec `git bash` ou `putty`

```
$ ssh monID@monAdresseIP
```

* Ouvrir le fichier d'authorisation de clés publiques suivant avec Nano 

:warning: si le répertoire `~/.ssh` n'existe pas, veuillez le créer

```
$ nano ~/.ssh/authorized_keys
```

* copier la clé publique ci-dessous dans une nouvelle ligne 

(attention copier la clé tel quel sans espace ou autre charactere, i.e. la clé est longue)

```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQD2pLhMqFGKffSdYvNCMAyM7598oBY+m/3q5AMXmb7IE6vq42+yGzqEUzZu9WrFckFD4Hq52rIU5DeOvi83DCF3uroXjNTEtCKdi+tY7cV18bHmsDsBHMqTnpuvroofgFWA0Pi++b2kGW2I5eyy1Qjv5rOp7y11Xe6XeZFEz7qQO1/xNiBMJEruG9Xldgooe4hkaOF39qnbqD4ui3LxYaTUTEulstw4wN70dSB8Zu9YQP7A7KU2zIEwJ1aw8whfO1CAM/AVvoDyqMtV8VXoaZSHOBgluMtinQfyyt473S2ZZeJlnmhK0F1gdOhO4SVZNRMj96m30ryYkYBFWvvLRP5N b300098957@ramena
```

## Identifiant

:two: Renseigner son utilisateur dans le tableau ci-dessous (i.e. MONUSER@10.13.237.126 => brice@10.13.237.126)

|:hash:| :id:      | Interne                 | ssh              | Docker Engine    | Unit :hash: |
|------|-----------|-------------------------|------------------|------------------|-------------|
| 01   | 300106677 - [<image src="https://avatars.githubusercontent.com/u/71027895?v=4" width=20 height=20></image>](https://github.com/Leonaldo1994) | `ssh lenoaldolinux@10.13.237.37`   |:heavy_check_mark:| :x: | :three::seven: |
| 02   | 300115206 - [<image src="https://avatars.githubusercontent.com/u/73952068?v=4" width=20 height=20></image>](https://github.com/itonga) | `ssh ntonga@10.13.237.?`   |:x:| :x:    |?|
| 03   | 300117811 - [<image src="https://avatars.githubusercontent.com/u/71027809?v=4" width=20 height=20></image>](https://github.com/sio-mh)  |  `ssh sio-mh@10.13.237.34`   |:x:| :x: | :three::four:|            
| 04   | 300121460 - [<image src="https://avatars.githubusercontent.com/u/71027883?v=4" width=20 height=20></image>](https://github.com/daveinfo20) | `ssh dave21@10.13.237.31`   |:heavy_check_mark:| :x: | :three::one:| 
| 05   | 300122014 - [<image src="https://avatars.githubusercontent.com/u/71392439?v=4" width=20 height=20></image>](https://github.com/sylvainEmm) |`ssh ?@10.13.237.38`   |:x:| :x: | :three::eight: |


### [Participation](.scripts/Participation.md)

:three: Installer Docker Engine sur sa machine Linux

- [ ] Suivre le tutoriel suivant

[Installation de Docker Engine](https://github.com/CollegeBoreal/Tutoriels/tree/main/2.MicroServices/1.Containers/2.Docker/1.Engine/2.Linux)

- [ ] Vérifier que `Docker Engine` est installé sur sa machine

:m: en lançant la commande `docker container`

```
$ docker container ls
```

:m: en vérifiant que le service `docker engine` tourne

```
$ systemctl status docker
● docker.service - Docker Application Container Engine
   Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
   Active: active (running) since Tue 2019-10-08 17:23:47 UTC; 1 day 23h ago
     Docs: https://docs.docker.com
 Main PID: 24174 (dockerd)
    Tasks: 26
   CGroup: /system.slice/docker.service
           └─24174 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

Oct 08 17:23:44 300098957 dockerd[24174]: time="2019-10-08T17:23:44.382151023Z" level=warning msg="Your kernel does not support swap memory limit"
Oct 08 17:23:44 300098957 dockerd[24174]: time="2019-10-08T17:23:44.382179791Z" level=warning msg="Your kernel does not support cgroup rt period"
Oct 08 17:23:44 300098957 dockerd[24174]: time="2019-10-08T17:23:44.382190586Z" level=warning msg="Your kernel does not support cgroup rt runtime"
Oct 08 17:23:44 300098957 dockerd[24174]: time="2019-10-08T17:23:44.382361631Z" level=info msg="Loading containers: start."
Oct 08 17:23:45 300098957 dockerd[24174]: time="2019-10-08T17:23:45.084064004Z" level=info msg="Default bridge (docker0) is assigned with an IP address 172.17.0.0/16. Daemon 
Oct 08 17:23:45 300098957 dockerd[24174]: time="2019-10-08T17:23:45.412643470Z" level=info msg="Loading containers: done."
Oct 08 17:23:46 300098957 dockerd[24174]: time="2019-10-08T17:23:46.830608514Z" level=info msg="Docker daemon" commit=6a30dfc graphdriver(s)=overlay2 version=19.03.2
Oct 08 17:23:46 300098957 dockerd[24174]: time="2019-10-08T17:23:46.830955345Z" level=info msg="Daemon has completed initialization"
Oct 08 17:23:47 300098957 dockerd[24174]: time="2019-10-08T17:23:47.022365319Z" level=info msg="API listen on /var/run/docker.sock"
Oct 08 17:23:47 300098957 systemd[1]: Started Docker Application Container Engine.
```


