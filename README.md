# docker-node

# DEPRECATED
Please use images from this repo : https://gitlab.com/kgaut/docker-node-images

The registry is : https://gitlab.com/kgaut/docker-node-images/container_registry

Docker image to mangage node js task for dev and CI / CD.

Used to manage gulp task on my dev environment without the need to install nodejs on my machine and having to deal with multiple versions issues.

Also usefull for CI / CD tasks to generate assets within a docker container.

See https://hub.docker.com/repository/docker/kgaut/node

# Usage with docker

in a terminal, cd to your app directory and launch the container
```
docker run -t -i -v $(eval pwd):/app kgaut/node:13 bash
```
It will mount your current directory within the `/app` container directory and open a ssh connexion inside this folder.

Then you'll be abble to launch the needed task. i.e. : 

```
npm ci
gulp build
```

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
docker-compose exec node npm ci
docker-compose exec node gulp build
```
