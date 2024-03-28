DOCKER

// Note:
Docker ps -a : All container
Docker ps: container is running
Docker logs: Log

Create a container for mysql
//Create Image mysql :
// 1 image => multiple containers
-d : Detach (background) mode
-e : environment variables






docker run \
-e	MYSQL_ROOT_PASSWORD=YOUR_PASSWORD\
—name mysql8-container\
-p 3308:3306\
-v mysql8-volume:/(path - thư mục chứa db trên container) \
-d mysql:8.0.28






//check Image
docker images

//Connect mysql throw your Host (PC, Laptop, …)
Mysql —protocol=tcp -h localhost -P 3308 -u root -p

//Go to inside the container
-it : interactive mode
docker exec -it CONTAINER_ID bash

AlTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password By 'YOUR_PASSWORD'
