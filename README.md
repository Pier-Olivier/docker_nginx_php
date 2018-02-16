# docker_nginx_php
small stack with 1 nginx in front to catch all 80 entries and 1 nginx in back for php-fpm.

# pour lancer les environnements  front / back

cd back 
docker-compose up -d


cd front 
docker-compose up -d


# pour inspecter front/back
cd back ou cd front

docker-compose ps

docker-compose logs -f

# teste avec URL (nginx_front -> nginx_back -> php)
http://0.0.0.0/index.php


# inspect containers dans network

docker network ls
docker network inspect back_default


# arréter
cd back et cd front
docker-compose down
