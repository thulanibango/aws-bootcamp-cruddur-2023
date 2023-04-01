#Journal for Week 1 - Containersation
## The following is the required homework:
 
 ### Push and tag a image to DockerHub

Here I built an image using the dockerfile for the frontend, tagged it and pushed it. The following is a step by step process of how that was carried out:
Go to frontend-react-js direcory
```
  cd frontend-react-js
```
Build docker image
```
 docker build --pull --rm -f "frontend-react-js/Dockerfile" -t frontend_boot:latest "frontend-react-js"
 ```
 ![docker image build](images/image_created.png)
tag docker image
 ```
 docker tag frontend_boot tula02/frontend_boot:v1
 ```

Push docker image
```
docker push tula02/frontend_boot:v1
```
![push to docker hub and tag image ](images/image_detail.png)

### Implementing a Health check in the docker composer file
Health checks are meant to chek if resources are healthy. Here health checks are implemented in the docker compose file.
The health checks are implemented on each resouce that 
![Implementation of health checks using the docker compose file ](images/Health_check.png)

### Multi-stage building for a Dockerfile build

Here i built a multi-stage for a docker build. The highlighted underlined parts show the images built normally and the one using multi-stage build. The underlined red is the originally built and the green is the multi-stage built, which shows it's advantages of speed and less space consumption. The steps to build the images are 
```
docker build -t demo:small .
```
![Mult-istage build for docker ](images/multistage_docker.png)

### Multi-stage building for a Dockerfile build

