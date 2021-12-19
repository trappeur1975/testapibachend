commande pour excuter le serveur web de symfony :
    symfony server:start --port=8080
    Dans son navigateur aller a l adresse : http://127.0.0.1:8080

commande pour excuter les fixtures :
    cette commande vide totalement la base de données avant d'insérer les nouvelles données:
        php bin/console doctrine:fixtures:load
dans le fichier "composer.json" un script (que j ai nommé « reset-data ») a été crée pour remettre a zero ma base de donnée, surtout utile pour l'utilisation d'un jeu de donnée via des fixtures. Pour l executer il suffit d'executer la commande suivante :
            
            composer reset-data
  
    apres il faudra creer un dossier "migrations" a la racine du projet si il n'existe pas
    puis lancer les commandes suivantes :
        php bin/console doctrine:migrations:generate
        php bin/console make:migration
        php bin/console doctrine:migrations:migrate

----------------------------
18/12/2021 : version 1 sans jwt
19/12/2021 : jwt installer2
19/12/2021 : modification du fichier security.yaml