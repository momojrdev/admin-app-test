**********************Outils utilises**********************
java 17

Docker

maven
***************************************Utilisation des services pour configurer Docker Compose**************************************
Le fichier docker-compose.yml spécifie la configuration des services Docker. Voici une vue d'ensemble de la configuration :

# Service PhpMyAdmin (phpmyadmin-admin-db):

<img width="349" alt="php my admin" src="https://github.com/momojrdev/admin-app-test/assets/123044247/63ea6cd9-e59c-4da9-b3a9-af3805e60a02">
Ce service exploite la version la plus récente de l'image Docker de PhpMyAdmin, et il requiert la présence du service MySQL. Il est paramétré pour établir une connexion avec le serveur MySQL. L'accès à PhpMyAdmin est possible depuis l'hôte via le port 8085.


# Service MySQL (mysql-admin-db):
<img width="482" alt="mysql-admin" src="https://github.com/momojrdev/admin-app-test/assets/123044247/a4ef902b-4007-4269-a5f1-c107548731d0">

Ce service repose sur l'image Docker de MySQL, version 8.0, et génère une base de données avec les paramètres d'identification suivants :

Utilisateur MySQL : user
Mot de passe MySQL : user
Base de données MySQL : adminapp-db
Le conteneur expose le port 3306 afin de faciliter la connexion depuis l'hôte. Les données MySQL sont persistantes et enregistrées dans un volume désigné sous le nom de "mysql_data".
De plus, le service intègre une vérification de la santé qui utilise la commande mysqladmin ping pour garantir la disponibilité de MySQL.
# Volumes
<img width="395" alt="volumes" src="https://github.com/momojrdev/admin-app-test/assets/123044247/1c55de82-6768-485f-8c25-2f0381dac50a">
Les volumes Docker sont comme des boîtes de stockage qui gardent les données même quand les boîtes (les conteneurs) sont fermées. Ici, dans ce projet, le volume "mysql_data" est utilisé pour garder les données de MySQL de façon durable. Cela veut dire que les données restent intactes même si le conteneur est éteint, évitant ainsi toute perte de données.


***********************Methoddologie a suivre ***********************


<img width="932" alt="pulling" src="https://github.com/momojrdev/admin-app-test/assets/123044247/38d7310e-2e62-4ec5-8714-c8dfb5b068f1">



<img width="758" alt="docker exec" src="https://github.com/momojrdev/admin-app-test/assets/123044247/ddda1f04-856b-4e8f-b966-f64927d6ec67">





<img width="613" alt="show tables" src="https://github.com/momojrdev/admin-app-test/assets/123044247/83b38c03-331c-40e4-b8f2-d82b3aa5fe85">

***************************Voici la base qui a ete cree**************************




<img width="959" alt="databas addmiin" src="https://github.com/momojrdev/admin-app-test/assets/123044247/67486505-5820-43ca-ac69-b384ab4b7d02">



