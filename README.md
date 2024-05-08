
### Creer les volume en local


```
mkdir mysql-data
```

```
mkdir front-data
```


### Lancer les docker-compose


```
docker-compose up
```

```
docker compose up
```

### NB : JE N'AI BESOIN DE RIEN CREER SA CREER LE RESEAU JE LANCE JUSTE LES COMMADES ET SA MARCHE

### Explication


ici les container front e back vont comminiquer entre eux seulement si je lance sa dans la macchine docker qui a l'adress ip 192.168.56.14
donc lors de la masterclass les gar doivent installer la meme machine docker pour pouvoir faire functioner les container  # dockercompose-frontangular-backspring-fonctionant-back

pour deployer dans une autre machine tu utilise ce lien pour cloner et lancer la nouvel build de l'image en mettant l'adress ip de la nouvelle machine dans config et sa doit etre sous la 
forme http://nouvel_ip:8080 pour pouvoir communiquer avec le back end 
```
git clone https://github.com/stevymonkam/EcomerceFinal.git
```

