iptables
====

Le rôle iptables permet d'authoriser la communication avec les machines externes en utilisant le protocole et via les ports passés en paramètres.

Version: v0.2

paramètres
------------

Ce rôle prends trois paramètres : 
 
 - protocol : le protocole de communication  

 - ports :  le tableau contenant les ports à ouvrir.  

 - comment : une chaine de caractères pour mettre dans le commentaire le nom du module/flux pour lequel on veut ovrir le/les port(s)  


Exemples d'utilisation
----------------

- Dans un rôle (dans le main.yml de meta)

```
dependencies:
  - {role: iptables, comment: "component", protocol: tcp, ports: [8080] } 
```

- Dans une playbook

```
roles:
  - {role: iptables, comment: "component", protocol: tcp, ports: [8080] }
```
