
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
git clone https://github.com/stevymonkam/ecommerce-angular.git
```

si l' adrees ip de la macchine docker a changer voici ce qu'il faut faire pour remettre l'adress ip

vi /etc/sysconfig/network-scripts/ifcfg-enp0s8


DEVICE=enp0s8
BOOTPROTO=none
ONBOOT=yes
IPADDR=192.168.1.100  # Remplacez ceci par votre adresse IP souhaitée tu change par l'adress ip que tu veux
NETMASK=255.255.255.0  # Remplacez ceci par votre masque de sous-réseau
GATEWAY=192.168.1.1    # Remplacez ceci par votre passerelle par défaut


Tous le reste tu le met comsa dans le fichier voici la seule chose a changer IPADDR=192.168.1.100 en fonction de seke tu veux le reste tu met comme s est exact il peut arriver que le BOOTPROTO=dhcp tu le met comsa BOOTPROTO=none
Et s'il ya pas le reste la tu ajoute car il peut arriver qu'il ya pas 
IPADDR=192.168.1.100  #
NETMASK=255.255.255.0  # 
GATEWAY=192.168.1.1    # 

Si c est le cas tu remet exact comsa

Apres 

sudo systemctl restart network
sudo systemctl daemon-reload
sudo service docker restart
![image](https://github.com/stevymonkam/dockercompose-frontangular-backspring-fonctionant-back/assets/65792571/7b61dd91-7065-4291-847b-6ddab2114d6a)


