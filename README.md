# spring-boot-mongodb
This repository contains a Spring Boot example project for MongoDB.

For a code review of this repo, see my related [blog post](https://springframework.guru/3402-2/).

You can learn more about my courses [here](http://courses.springframework.guru/courses/) on my site.

# mongodb server host connect
For windows use docker-machine IP ( docker-machine.exe ip) to connect to mongo database 
192.168.99.102:27017

To save data after container is stopped, we created a volume. Mounting node not working on windows.
docker volume create --name=mongodbvolume

docker run -p 27017:27017 -v mongodbvolume:/data/db -d mongo

#RabbitMQ
docker run -d --hostname my-rabbit --name some-rabbit -p 5671:5671 -p 5672:5672 -p 8080:15672 -v D:/dockerdata/rabbitmq rabbitmq:3-management