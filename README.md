#symfony-docker-apache
Docker setup for symfony using apache. The docker engine version used is 19.03.5.
The symfony version is the LTS 4.4.x of the framework and also minimal install generated by 
running:

    docker-compose run composer create-project symfony/skeleton . 4.4.x
    
Besides symfony postgres is provisioned and mailhog, please get more information by looking at the docker-compose.yml 
file

##Installation
Clone the repository and run

    docker-compose up -d

##Usage

You should be able to see the welcome page by visiting your browser on 127.0.0.1:8080
    
Other deps can be installed using composer in the same way, e.g. using composer flex extension:

    docker-compose run composer require twig
    docker-compose run composer require doctrine
    docker-compose run composer require maker
    
The console, e.g. can be used as follows:

    docker-compose exec php bin/console
    docker-compose exec php bin/console cache:clear
    docker-compose exec php bin/console make:controller MyController
    

Enjoy :-)

