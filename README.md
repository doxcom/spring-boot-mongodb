# spring-boot-mongodb
This repository contains a Spring Boot example project for MongoDB.

For a code review of this repo, see my related [blog post](https://springframework.guru/3402-2/).

You can learn more about my courses [here](http://courses.springframework.guru/courses/) on my site.


- to apply persistence:
docker run -p 27017_27017 -v /dockerdata/mongo/:/data/db -d mongo

- to run mysql docker img 
inside C:\Users\mitno I created a folder named temp, and then:

- docker run --name aldo2-mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -v /temp:/var/lib/mysql -p 3306:3306 -d mysql


# Centos with java#
run image
- docker run -d centos tail -f /dev/null
get the name:
  CONTAINER ID   IMAGE     COMMAND               CREATED         STATUS         PORTS     NAMES
  eba557f3c4f6   centos    "tail -f /dev/null"   4 seconds ago   Up 3 seconds             unruffled_bardeen

execute a terminal inside centOS:
- docker exec -it unruffled_bardeen bash
unruffled_bardeen is the name of the container

try:
-yum install java
if it fails

try:

FROM centos

cd /etc/yum.repos.d/
sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

yum -y install java


#Install MySQL
https://dev.mysql.com/downloads/file/?id=534098

On Centos
- yum update
- yum install wget
- wget https://dev.mysql.com/get/mysql80-community-release-el7-3.noarch.rpm
- get the .rpm name file and:
- rpm -ivh mysql80-community-release-el7-3.noarch.rpm
- yum install mysql-server

