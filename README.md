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
1. Prepare private and public network
2. Prepare one dockerfile based on ubuntu with the ping command
3. One container must have access to the private and public networks the second container
must be in the private network
4. A ) Run a container that has access to the public network and ping some resources (
example: google.com )
B ) The second container ping the first container via a private network
5. Report save in GitHub repository
