# Docker Commands Cheatsheet and Reference

This document provides an overview of the most important Docker commands that you'll commonly use when working with Docker.

## Docker Container Commands

| Command                                   | Description                                    |
| ----------------------------------------- | ---------------------------------------------- |
| `docker run <image>`                    | Create and start a new container from an image |
| `docker start <container>`              | Start an existing, stopped container           |
| `docker stop <container>`               | Stop a running container                       |
| `docker pause <container>`              | Pause all processes within a container         |
| `docker unpause <container>`            | Unpause a paused container                     |
| `docker kill <container>`               | Kill a running container (sends SIGKILL)       |
| `docker rm <container>`                 | Remove a stopped container                     |
| `docker exec -it <container> <command>` | Execute a command in a running container       |

## Docker Image Commands

| Command                     | Description                                                  |
| --------------------------- | ------------------------------------------------------------ |
| `docker build -t <tag> .` | Build a new image from a Dockerfile in the current directory |
| `docker images`           | List all local images                                        |
| `docker pull <image>`     | Pull an image from a registry                                |
| `docker push <image>`     | Push an image to a registry                                  |
| `docker rmi <image>`      | Remove a local image                                         |
| `docker image prune`      | Remove all unused images                                     |

## Docker Network Commands

| Command                                             | Description                           |
| --------------------------------------------------- | ------------------------------------- |
| `docker network create <network>`                 | Create a new network                  |
| `docker network ls`                               | List all networks                     |
| `docker network inspect <network>`                | Inspect a network                     |
| `docker network connect <network> <container>`    | Connect a container to a network      |
| `docker network disconnect <network> <container>` | Disconnect a container from a network |
| `docker network rm <network>`                     | Remove a network                      |

## Docker Volume Commands

| Command                            | Description               |
| ---------------------------------- | ------------------------- |
| `docker volume create <volume>`  | Create a new volume       |
| `docker volume ls`               | List all volumes          |
| `docker volume inspect <volume>` | Inspect a volume          |
| `docker volume rm <volume>`      | Remove a volume           |
| `docker volume prune`            | Remove all unused volumes |

## Docker Compose Commands

| Command                                     | Description                                         |
| ------------------------------------------- | --------------------------------------------------- |
| `docker-compose up -d`                    | Start all services in detached mode                 |
| `docker-compose down`                     | Stop and remove all services, networks, and volumes |
| `docker-compose logs -f`                  | Follow logs for all services                        |
| `docker-compose ps`                       | List all running services                           |
| `docker-compose exec <service> <command>` | Execute a command in a running service container    |

This cheatsheet covers the most commonly used Docker commands. For more detailed information, refer to the official [Docker documentation](https://docs.docker.com/engine/reference/commandline/).
