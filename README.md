# spring-boot-mongodb
This repository contains a Spring Boot example project for MongoDB.

For a code review of this repo, see my related [blog post](https://springframework.guru/3402-2/).

You can learn more about my courses [here](http://courses.springframework.guru/courses/) on my site.


- to apply persistence:
docker run -p 27017_27017 -v /dockerdata/mongo/:/data/db -d mongo

- to run mysql docker img 
inside C:\Users\mitno I created a folder named temp, and then:

- docker run --name aldo2-mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -v /temp:/var/lib/mysql -p 3306:3306 -d mysql