# Docker Commands Cheatsheet and Reference

This document provides an overview of the most important Docker commands and concepts that are commonly asked about in interviews.

## Docker Fundamentals

### What is Docker?

Docker is an open-source platform for building, deploying, and managing containerized applications. It allows developers to package their applications and dependencies into a standardized unit called a container, which can then be easily distributed and run on any system.

### Key Docker Concepts

- **Image**: A read-only template used to create containers. Contains the application code, dependencies, and other necessary files.
- **Container**: A runnable instance of an image. Containers are isolated, lightweight, and portable.
- **Registry**: A central store for Docker images. The most common is Docker Hub, a public registry provided by Docker.
- **Dockerfile**: A text file that contains the instructions for building a Docker image.
- **Volumes**: A way to persist data generated by a container, independent of the container's lifecycle.
- **Networks**: Allows containers to communicate with each other and the outside world.
- **Docker Compose**: A tool for defining and running multi-container Docker applications.

## Important Docker Commands

### Docker Container Commands

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

### Docker Image Commands

| Command                     | Description                                                  |
| --------------------------- | ------------------------------------------------------------ |
| `docker build -t <tag> .` | Build a new image from a Dockerfile in the current directory |
| `docker images`           | List all local images                                        |
| `docker pull <image>`     | Pull an image from a registry                                |
| `docker push <image>`     | Push an image to a registry                                  |
| `docker rmi <image>`      | Remove a local image                                         |
| `docker image prune`      | Remove all unused images                                     |

### Docker Network Commands

| Command                                             | Description                           |
| --------------------------------------------------- | ------------------------------------- |
| `docker network create <network>`                 | Create a new network                  |
| `docker network ls`                               | List all networks                     |
| `docker network inspect <network>`                | Inspect a network                     |
| `docker network connect <network> <container>`    | Connect a container to a network      |
| `docker network disconnect <network> <container>` | Disconnect a container from a network |
| `docker network rm <network>`                     | Remove a network                      |

### Docker Volume Commands

| Command                            | Description               |
| ---------------------------------- | ------------------------- |
| `docker volume create <volume>`  | Create a new volume       |
| `docker volume ls`               | List all volumes          |
| `docker volume inspect <volume>` | Inspect a volume          |
| `docker volume rm <volume>`      | Remove a volume           |
| `docker volume prune`            | Remove all unused volumes |

### Docker Compose Commands

| Command                                     | Description                                         |
| ------------------------------------------- | --------------------------------------------------- |
| `docker-compose up -d`                    | Start all services in detached mode                 |
| `docker-compose down`                     | Stop and remove all services, networks, and volumes |
| `docker-compose logs -f`                  | Follow logs for all services                        |
| `docker-compose ps`                       | List all running services                           |
| `docker-compose exec <service> <command>` | Execute a command in a running service container    |

This cheatsheet covers the most commonly used Docker commands. For more detailed information, refer to the official [Docker documentation](https://docs.docker.com/engine/reference/commandline/).

## Docker Best Practices

- **Use Minimal Base Images**: Start with a minimal base image (e.g., `alpine` or `scratch`) to reduce the image size and attack surface.
- **Utilize Multi-Stage Builds**: Use multi-stage builds to optimize image size by only including the necessary build artifacts.
- **Leverage Environment Variables**: Use environment variables for configuration to make your containers more portable.
- **Implement Health Checks**: Add health check commands to ensure your containers are running correctly.
- **Manage Secrets Securely**: Use tools like Docker Secrets or environment variables to store sensitive information.
- **Avoid Installing Unnecessary Packages**: Only install packages that are required for your application to run.
- **Minimize Layers in Dockerfile**: Consolidate instructions in your Dockerfile to reduce the number of layers.
- **Tag Images Consistently**: Use a consistent naming and tagging convention for your Docker images.

## Common Docker Interview Questions

* **Explain the difference between a Docker container and a virtual machine.**

  <details>
  <summary>Answer</summary>
  Containers are lightweight, run on the host's operating system, and share the host's kernel. VMs are full-blown operating systems that run on top of a hypervisor.
  </details>
* **What is a Dockerfile and how do you use it to build a Docker image?**

  <details>
  <summary>Answer</summary>
  A Dockerfile is a text file that contains instructions for building a Docker image. You use the `docker build` command to build an image from a Dockerfile.
  </details>
* **How do you manage data persistence in Docker containers using volumes?**

  <details>
  <summary>Answer</summary>
  Volumes are the preferred way to persist data in Docker. They allow you to decouple data from the container lifecycle and store it on the host file system.
  </details>
* **Describe the Docker networking model and the different types of networks.**

  <details>
  <summary>Answer</summary>
  Docker provides several network drivers, including bridge, host, overlay, and macvlan. These allow containers to communicate with each other and the outside world.
  </details>
* **Explain the purpose of Docker Compose and how it's used to manage multi-container applications.**

  <details>
  <summary>Answer</summary>
  Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to specify the services, networks, and volumes in a YAML file, making it easier to deploy complex applications.
  </details>
* **What are some best practices for building efficient and secure Docker images?**

  <details>
  <summary>Answer</summary>
  Best practices include using minimal base images, implementing multi-stage builds, managing secrets securely, and avoiding installing unnecessary packages.
  </details>
* **How do you handle environment-specific configurations in Docker-based applications?**

  <details>
  <summary>Answer</summary>
  You can use environment variables to store configuration settings and make your containers more portable across different environments.
  </details>
* **Describe the process of deploying a Docker-based application to a production environment.**

  <details>
  <summary>Answer</summary>
  The process typically involves building Docker images, pushing them to a registry, and then using orchestration tools like Kubernetes or Docker Swarm to deploy the application to production.
  </details>
* **Explain the concept of Docker registry and how it's used to store and distribute Docker images.**

  <details>
  <summary>Answer</summary>
  A Docker registry is a centralized store for Docker images. The most popular is Docker Hub, which allows you to host and distribute your own Docker images.
  </details>
* **How do you debug and troubleshoot issues within a running Docker container?**

  <details>
  <summary>Answer</summary>
  You can use commands like `docker logs`, `docker exec`, and `docker inspect` to view logs, execute commands, and inspect the state of a running container.
  </details>
