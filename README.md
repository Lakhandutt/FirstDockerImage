# FirstDockerImage

# DockerAngularApp

This project is about creating the docker Image of Angular app

## Getting Started

Docker file is present in the angularapp folder and described as well

### Prerequisites

Install 1.nodejs 2. npm 3.angular cli 4.Docker and  

```
Follow the offical documentations according to Operating system
```

### Installing

Clone the repo and run following commands:

```
npm install
```

now create docker image
```
docker build --rm -f angularapp/Dockerfile -t angularapp:v1 angularapp
```
Run docker image
```
docker run --rm -d -p 80:80 angularapp:v1
```
stop docker container
```
 docker ps
 ```
 ```
  docker stop 58ba2953c0e5
```
push it to dockerhub 1. tag the image
```
docker tag angularapp:v1 <dockerid>/angularapp:v1 
```
```
docker login
``` 
push the image
```
 docker push lakhandutt/angularapp:v1
```
```
docker image ls
```

## Versioning
Current version : V1