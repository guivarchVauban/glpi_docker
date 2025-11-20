# GLPI Docker

Installation de glpi à l'aide de Docker basé sur https://hub.docker.com/r/diouxx/glpi

Le docker-compose proposé ici est celui avec persistance de données décrit dans la partie **Deploy with persistence data**

## Execution

1. Cloner le dépot : `git clone https://github.com/guivarchVauban/glpi_docker.git`
2. Modifier le fichier mariadb.env pour personnaliser vos mots de passe

3. Lancer
  ``` docker-compose up -d ``` pour lancer en mode détaché (rend la main sur le shell)
ou 
 ``` docker-compose up ```

## Containers lancés

### Mariadb 10.7 pour la base de données

 Attention : Pour la persitence de données le docker utilisera le dossier ```/var/lib/mysql``` de la machine hôte

 ***Le nom d'hote de la machine ```mariadb``` sera a utiliser lors de la configuration initiale de glpi (première installation) dans le champ "SQL Server".***


### GLPI (basé sur diouxx/glpi)

 Port exposé : 80 (http)

## Accès

http://@IP_de_la_machine_hote

***Après la première installation, penser à supprimer le fichier install/install.phps dans /var/www/html/glpi***

Les comptes par défaut sont :

- glpi/glpi 
- tech/tech technical 
- normal/normal 
- post-only/postonly
