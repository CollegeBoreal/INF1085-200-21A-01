# docker-machine

- [ ] Installer une machine Générique

https://github.com/CollegeBoreal/Tutoriels/tree/main/2.MicroServices/2.VM/1.Docker-Machine/


<img src="images/docker-machine.png.png" width=412 height=231 > </img>


- [ ] Lister les machines 

```
docker-machine ls
```
> Retour
```
NAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER      ERRORS
ma-machine   -     generic      Running   tcp://10.13.237.25:2376             v19.03.12  
```

- [ ] Activer une machine

```
eval $(docker-machine env ma-machine)
```

- [ ] Visualiser les machines actives

* toutes les machines Note: :star:

```
docker-machine ls
```
> Retour
```
NAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER      ERRORS
ma-machine   *     generic      Running   tcp://10.13.237.25:2376             v19.03.12  
```

* la machine active

```
docker-machine active
```
> Retour
```
ma-machine
```

- [ ] Annuler les machines actives

```
eval $(docker-machine env --unset)
```
