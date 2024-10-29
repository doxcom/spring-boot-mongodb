# Spring-boot-mongodb
This repository contains a Spring Boot example project for MongoDB.

For a code review of this repo, see my related [blog post](https://springframework.guru/3402-2/).

You can learn more about my courses [here](http://courses.springframework.guru/courses/) on my site.


#To do persist on Windows,

-Install docker desktop

-on terminal try: docker pull mongo

- select a folder in your C/ disk, C:\Users\YourWindowsUserName\

- inside create a folder, example C:\Users\mitno\mongostoragepractice

-inside that folder run: docker run -p 27017:27017 -v /dockerdata/mongo/:/data/db -d mongo

- docker it will create the directory dockerdata/mongo belongs to your machine, and the /data/db belongs inside the 
container

-check with docker ps:
PS C:\Users\mitno\mongostoragedocker> docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                      NAMES
77a220f133ca   mongo     "docker-entrypoint.s…"   7 seconds ago   Up 6 seconds   0.0.0.0:27017->27017/tcp   kind_kowalevski

-run your springboot application : src/main/java/guru/springframework/SpringBootMongodbApplication.java

- check : http://localhost:8080/product/list

- if there is no prods add new ones, then stop the container: get the container id with docker ps command, and then 
use docker stop 96c17f479beb(this is the containerID)
- run again: docker run -p 27017:27017 -v /dockerdata/mongo/:/data/db -d mongo
- check again: http://localhost:8080/product/list you will see the products, this means mongodb has persistence