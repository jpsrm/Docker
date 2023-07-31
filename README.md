### Docker installation on Ubuntu

    *  apt update
    *  apt-get install docker
    *  apt  install docker.io 
---

## Docker File Configuration for creating a container image
### Commands
    *  mkdir docker1
    *  cd docker1
    *  vim Dockerfile
---

### Docker File Creation Commands

    FROM ubuntu:latest
    RUN apt-get update
    RUN apt-get install nginx -y
    RUN service nginx start
    RUN mkdir dockers
    RUN cd dockers
    WORKDIR dockers
    EXPOSE 80
---
### Docker Image creation using Dockerfile 

    docker build -t image1 .
---
### Container Creation 

     docker container run -it --name <Container_name> -p <Port_no> <Image_Name> /bin/bash
Example
     
     docker container run -it --name con -p 8080:80 image1 /bin/bash
---

### Container open Command

     docker exec -it con /bin/bash
---

### Docker Hub Login
    docker login
    username
    password
---

### container push commands
    docker tag image2 mohan223/contain:image1
    docker push mohan223/contain:image1
---

### Container pull command
    docker pull mohan223/contain:image1








     
