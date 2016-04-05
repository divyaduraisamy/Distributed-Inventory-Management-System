# Distributed-Inventory-Management-System
The project involves three different scenarios , one fo the scenarios whose docker-compose is porvided is ,
  1. Customer places an order in a web application , providing details of his address and his/her requirement. 
     GeoLocation API of google is used to fix the latitude and longitude of the address and request is sent to another container 
     which contains the services , "PlaceOrderToStore" service is called , which accesses the database of the stores nearby and provide the list
     of stores and availability to user
     
     Docker commands are ,
     
     Dockerfile of customer is run 
     ```bash
docker run -d app/client

 ``` 
 Dockerfile of service is run
    ```bash
docker run -d app/service

 ``` 
 MySql Docker container is built
    ```bash

docker pull tutum/mysql:5.5
docker run -d -p 3306:3306 -v /tmp:/tmp  -e STARTUP_SQL="/db/Inventory.mysql"
 ``` 
 The Docker-compose.yml is run
    ```bash

docker-compose up -d

 ```
 
 
 
 
  
