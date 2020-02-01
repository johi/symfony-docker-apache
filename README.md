#symfony-docker-apache
Docker setup for symfony using apache. The symfony code is the minimum generated for the LTS 4.4.x of the framework by 
running:

    docker-compose run composer create-project symfony/skeleton . 4.4.x
    
Other deps can be installed using composer in the same way, e.g. using composer flex extension:

    docker-compose run composer require twig
    docker-compose run composer require doctrine
    docker-compose run composer require maker
    
The console, e.g. can be used as follows:

    docker-compose exec php bin/console
    docker-compose exec php bin/console cache:clear
    docker-compose exec php bin/console make:controller MyController
    
Enjoy :-)

