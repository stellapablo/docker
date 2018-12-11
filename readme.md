#Goals


1. Run a dev enviroment in Docker
  Nginx/PHP
  Mysql
  Redis

2. Dockerfile to build a nginx/php image

3. Re use existing images for MySQL/Redis


docker build -t shippingdocker/app:latest -f app/Dockerfile docker/app
docker build -t shippingdocker/app:latest -f app/Dockerfile docker/app
docker build -t shippingdocker/app:latest -f app/Dockerfile 
docker build -t shippingdocker/app:latest -f docker/app
docker build -t shippingdocker/app:latest -f docker/app/Dockerfile  docker/app
cd /home/pablo/docker/
docker build -t shippingdocker/app:latest -f docker/app/Dockerfile  docker/app
cd docker/
docker run --name=app --network=appnet -d --rm -p 81:80 -v $(pwd)/application:/var/www/html/public shippingdocker/app:latest 
docker ps
docker stop app 
docker run --name=app --network=appnet -d --rm -p 81:80 -v $(pwd)/application:/var/www/html/ shippingdocker/app:latest 
docker ps
docker exec -it app bash
docker run --rm -d --name=mysql --network=appnet -v mydata:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=homestead -e MYSQL_USER=homestead -e MYSQL_USER_PASSWORD=secret mysql:5.
docker ps
docker exec -it mysql bash
docker exec -it app bash
docker volume ls
docker kill mysql
docker run --rm -d --name=mysql --network=appnet -v mydata:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=homestead -e MYSQL_USER=homestead -e MYSQL_USER_PASSWORD=secret mysql:5.7
docker exec -it mysql bash
docker ps
docker inspect mysql
docker-compose ps
docker-compose --version
docker-compose ps
docker --version
docker-compose up -d

