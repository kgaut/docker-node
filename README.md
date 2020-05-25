# docker-node
Docker image to mangage node js task for dev and CI / CD.

Used to manage gulp task on my dev environment without the need to install nodejs on my machine and having to deal with multiple versions issues.

Also usefull for CI / CD tasks to generate assets within a docker container.

See https://hub.docker.com/repository/docker/kgaut/node

## Usage with docker-compose

Add to your docker-compose.yml :
```
  node:
    image: kgaut/node:13
    container_name: "myproject_nodejs"
    volumes:
      - ./:/app
    tty: true
  ```
  
  Launch the containers : 
  ```
  docker-compose up -d 
  ```
  
  Then launch the needed tasks within the container, for example : 
  ```
  docker-compose exec -T node npm ci
  docker-compose exec -T node gulp build
  ```
