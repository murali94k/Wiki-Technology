## Docker Basics 
| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `docker build -t <image_name> .`                           | build new image from Dockerfile and tag                                                 |
| `docker build -t <image_name> .`  | |
| ` docker images` | List all images |
| `docker run -p host:container_port -d --name <container_name> <image_name>` | Run the images in container |
| `docker ps -a` | show all containers |
|`docker stop <container_id>`| |
|`docker start <container_id>`| |
| `docker exec -it <container_name> /bin/bash`| Exec into the container |
|`docker cp ./sqldump.sql <container_name>:/tmp/`| Copy file from local into the container tmp dir|

## Remove images/containers

| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
|`docker rm -f <container_id>` | Force Remove container |
|`docker rmi -f <image_name>`| Force remove image |
|`docker system prune --all` | Force remove all containers/ images |

## Docker Network

<img src="./images/docker_network_1.jpg" alt="docker network" style="width:500px;"/>

| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `docker create network <network_name>` | Create new Bridge network |
| `docker network ls` | List all networks |
| `docker network connect <network_name> <container_name>` | Connect the container to be part of the network |
| `docker network disconnect <network_name> <container_name>` | |

## Docker Inspect
| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `docker network inspect <network_name> / <container_id>` | |

## Docker Run with a new bridge network
```
  docker run -it -d -p <host>:<container> --name <container_name> --net <network_name> <image_name>
```

> Note:
  CMD is executed at docker run stage but RUN is executed at docker build stage
	only the last CMD will be heeded
