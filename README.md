# Sayna-TestBack-PHP
Le projet d'api s'est fait par le framwork Symfony.

Hébergement : https://saynatestbackphp.herokuapp.com/

****************************************************************************************

Faut pas oublier dans les requettes get dans le Header : 
le paramètre :  Authorization : Clée Bearer générer par le token JWT après authentification utilisateur.

Route dans l'application : GET
Affichage de la page d'acceuil : 
- /

Authentification d'un utilisateur : POST 
Avec Body RAW {"username" : "xxxxx","password":"xxxxx"}
- /api/login_check

Inscription d'un utilisateur : POST
Avec Body RAW {"username" : "xxxxx","password":"xxxxx"}
- /register

Liste des utilisateurs : GET
- /api/users

Liste d'un utilisateur spécifique : GET
- /api/users/{id}

Liste des cartes : GET
- /api/bills

Liste d'une carte spécifique : GET
- /api/bills/{id}

Liste des musiques: GET
- /api/songs

Liste d'une music spécifique : GET
- /api/songs/{id}

Ajjout d'une music : POST
- /api/songs/post

****************************************************************************************

Après Clone du projet : 
Executez les actions suivantes dans le dossier contenant les sources:
Ouvrir un terminal dans ce chemins et executer dans le terminal : 
1 - composer install

Créer la base de donnée en local
Vérifier les identifiants dans le fichier .env
Pouy mysql : 
-DATABASE_URL="mysql://[identifiant]:[password]@127.0.0.1:3306/[dbName]?serverVersion=5.7"

Après taper dans le terminal
- php bin/console doctrine:database:create


Après executer les mgrations : 
- php bin/console make:migration
- php bin/console doctrine:migrations:migrate 


Executer le server de l'application dans le terminal par : 
- symfony serve
