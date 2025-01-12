# Fundamental Docker Commands for Managing Containers

## 1. `docker run`
- **Description**: Creates and starts a new container from a specified image.
- **Usage**: `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`
- **Example**: `docker run -d -p 80:80 nginx` (Runs an Nginx container in detached mode and maps port 80 of the host to port 80 of the container)

## 2. `docker ps`
- **Description**: Lists all running containers.
- **Usage**: `docker ps [OPTIONS]`
- **Example**: `docker ps -a` (Lists all containers, including stopped ones)

## 3. `docker stop`
- **Description**: Stops a running container.
- **Usage**: `docker stop [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker stop my_container` (Stops the container named `my_container`)

## 4. `docker start`
- **Description**: Starts a stopped container.
- **Usage**: `docker start [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker start my_container` (Starts the container named `my_container`)

## 5. `docker restart`
- **Description**: Restarts a running container.
- **Usage**: `docker restart [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker restart my_container` (Restarts the container named `my_container`)

## 6. `docker rm`
- **Description**: Removes one or more stopped containers.
- **Usage**: `docker rm [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker rm my_container` (Removes the container named `my_container`)

## 7. `docker exec`
- **Description**: Runs a command in a running container.
- **Usage**: `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`
- **Example**: `docker exec -it my_container /bin/bash` (Starts a bash session in the running container named `my_container`)

## 8. `docker logs`
- **Description**: Fetches the logs of a container.
- **Usage**: `docker logs [OPTIONS] CONTAINER`
- **Example**: `docker logs my_container` (Fetches the logs of the container named `my_container`)

## 9. `docker inspect`
- **Description**: Displays detailed information on one or more containers.
- **Usage**: `docker inspect [OPTIONS] NAME|ID [NAME|ID...]`
- **Example**: `docker inspect my_container` (Displays detailed information about the container named `my_container`)

## 10. `docker cp`
- **Description**: Copies files/folders between a container and the local filesystem.
- **Usage**: `docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|DEST_PATH|-`
- **Example**: `docker cp my_container:/path/to/file /local/path` (Copies a file from the container named `my_container` to the local filesystem)

## 11. `docker commit`
- **Description**: Creates a new image from a container's changes.
- **Usage**: `docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]`
- **Example**: `docker commit my_container my_image:latest` (Creates a new image named `my_image` with the tag `latest` from the container named `my_container`)

## 12. `docker attach`
- **Description**: Attaches local standard input, output, and error streams to a running container.
- **Usage**: `docker attach [OPTIONS] CONTAINER`
- **Example**: `docker attach my_container` (Attaches to the container named `my_container`)

## 13. `docker top`
- **Description**: Displays the running processes of a container.
- **Usage**: `docker top CONTAINER [ps OPTIONS]`
- **Example**: `docker top my_container` (Displays the running processes of the container named `my_container`)

## 14. `docker stats`
- **Description**: Displays a live stream of container(s) resource usage statistics.
- **Usage**: `docker stats [OPTIONS] [CONTAINER...]`
- **Example**: `docker stats my_container` (Displays resource usage statistics for the container named `my_container`)

## 15. `docker kill`
- **Description**: Kills one or more running containers.
- **Usage**: `docker kill [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker kill my_container` (Kills the container named `my_container`)

These commands cover the basic operations needed to manage Docker containers effectively.