# docker-tutorial
docker commands

//check version
docker -v
docker --version

//pull an image
docker pull image name

//search an image
docker search MySQL

//run an image
docker run OpenJDK


//view all docker images
docker ps
docker ps -a

docker run --name javaContainer -d 71260f256d19




1.`docker pull image name`

# Docker Commands Cheat Sheet

This document provides a quick reference for Docker commands from basic to advanced levels.

## Table of Contents

1. [Basic Commands](#basic-commands)
2. [Container Management](#container-management)
3. [Image Management](#image-management)
4. [Networking](#networking)
5. [Volume Management](#volume-management)
6. [Docker Compose](#docker-compose)
7. [Dockerfile](#dockerfile)
8. [Docker Registry](#docker-registry)

---

## Basic Commands

- **`docker version`**: Show Docker version and info.
- **`docker info`**: Display system-wide information about Docker.
- **`docker help`**: Get help on Docker commands.

## Container Management

- **`docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`**: Run a command in a new container.
  - Example: `docker run -it ubuntu bash`
- **`docker ps [OPTIONS]`**: List containers.
  - **`-a`**: Show all containers (default shows just running).
- **`docker start CONTAINER [CONTAINER...]`**: Start one or more stopped containers.
- **`docker stop CONTAINER [CONTAINER...]`**: Stop one or more running containers.
- **`docker restart CONTAINER [CONTAINER...]`**: Restart one or more containers.
- **`docker rm CONTAINER [CONTAINER...]`**: Remove one or more containers.
  - **`-f`**: Force removal of a running container.
- **`docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`**: Run a command in a running container.
  - Example: `docker exec -it mycontainer bash`

## Image Management

- **`docker images [OPTIONS] [REPOSITORY[:TAG]]`**: List images.
  - **`-a`**: Show all images (default hides intermediate images).
- **`docker pull IMAGE_NAME[:TAG]`**: Pull an image or a repository from a registry.
- **`docker rmi IMAGE_NAME[:TAG]`**: Remove one or more images.
  - **`-f`**: Force removal of the image.
- **`docker build [OPTIONS] PATH | URL | -`**: Build an image from a Dockerfile.

## Networking

- **`docker network ls`**: List networks.
- **`docker network create [OPTIONS] NETWORK`**: Create a network.
- **`docker network inspect NETWORK [NETWORK...]`**: Display detailed information on one or more networks.
- **`docker network connect NETWORK CONTAINER`**: Connect a container to a network.
- **`docker network disconnect NETWORK CONTAINER`**: Disconnect a container from a network.

## Volume Management

- **`docker volume ls`**: List volumes.
- **`docker volume create [OPTIONS] [VOLUME]`**: Create a volume.
- **`docker volume inspect VOLUME [VOLUME...]`**: Display detailed information on one or more volumes.
- **`docker volume rm VOLUME [VOLUME...]`**: Remove one or more volumes.

## Docker Compose

- **`docker-compose up [OPTIONS]`**: Build and start containers.
  - **`-d`**: Detached mode: Run containers in the background.
- **`docker-compose down [OPTIONS]`**: Stop and remove containers.
- **`docker-compose ps`**: List containers.
- **`docker-compose logs [SERVICE]`**: View output from containers.

## Dockerfile

- **`FROM IMAGE_NAME[:TAG]`**: Set the base image.
- **`RUN COMMAND`**: Execute a command in the container.
- **`COPY SRC DEST`**: Copy files from source to destination.
- **`CMD ["executable","param1","param2"]`**: Provide defaults for an executing container.

## Docker Registry

- **`docker login [OPTIONS] [SERVER]`**: Log in to a Docker registry.
- **`docker push IMAGE_NAME[:TAG]`**: Push an image or a repository to a registry.
- **`docker pull IMAGE_NAME[:TAG]`**: Pull an image or a repository from a registry.

---

This cheat sheet covers a range of Docker commands from basic container management to advanced Dockerfile usage and networking. For detailed options and more commands, refer to the Docker documentation at [docs.docker.com](https://docs.docker.com).
