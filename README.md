# GL_Homework10

Task 1
1. I installed Docker on EC2 instance according instruction from official site https://docs.docker.com/engine/install/ubuntu/
2. I prepared a dockerfile based on Apache image

  FROM httpd:2.4
  COPY index.html /usr/local/apache2/htdocs/
  EXPOSE 80

3. Added your own index.html page with your name and surname to the docker image
4. Run the docker container at port 8080
5. Open page in Web Browser
6. Report save in GitHub repository
