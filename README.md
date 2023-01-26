# GL_Homework10

## Task 1
1. I installed Docker on EC2 instance according instruction from official site https://docs.docker.com/engine/install/ubuntu/
2. I prepared dockerfile based on Apache image
```
  FROM httpd:2.4
  COPY index.html /usr/local/apache2/htdocs/
  EXPOSE 80
```
3. I made the image based on Dockerfile and run docker container at port 8080
![docker logs](https://user-images.githubusercontent.com/105345932/214928184-f10ad7af-e239-4bff-a61c-256343fa2786.png)

4. Result
![webpage](https://user-images.githubusercontent.com/105345932/214928570-5161203e-b9f2-45f8-bd89-a8d401c04b66.png)

## Task2
1. I prepared private and public networks

![creating networks](https://user-images.githubusercontent.com/105345932/214940065-2b42f5a5-f629-419c-b2b5-6f4b101aee99.png)

2. I prepared dockerfile based on ubuntu with the ping command
```
FROM ubuntu
RUN apt-get update && apt-get install -y iputils-ping
CMD bash

```
3. I created image based on Dockerfile

![create image2](https://user-images.githubusercontent.com/105345932/214941029-1520bedf-c53f-4b94-b4c8-abb42ad168ee.png)

4. I launched containers to the specified networks (node1 have access to the private and public networks, node2 have access only to private network)

![conecting networks and nodes2](https://user-images.githubusercontent.com/105345932/214941856-4ae46289-d2d0-421c-b8e3-7a33b9b73f25.png)

5. I checked ping from node1 to google.com and node2 

![ping from node1](https://user-images.githubusercontent.com/105345932/214942433-c80a2696-1ccb-4587-b624-f91b6f131edf.png)

6. I checked ping from node2 to google.com and node1 

![ping from node2](https://user-images.githubusercontent.com/105345932/214942573-36d3e132-7d47-4e27-9b20-1897f6e06bd8.png)

