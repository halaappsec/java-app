# java-app
https://github.com/spring-projects/spring-petclinic/tree/main

1- in root file 
start the database containers. Each one has a profile just like the Spring profile:

$ docker-compose --profile mysql up
or
$ docker-compose --profile postgres up

2- Building a Container
SPRING_PROFILES_ACTIVE=postgres ./mvnw spring-boot:build-image

2- Run a Container
docker run -it -p 8080:8080 spring-petclinic:3.1.0-SNAPSHOT

http://localhost:8080/
psql -h localhost -U petclinic -d petclinic
pass:petclinic
