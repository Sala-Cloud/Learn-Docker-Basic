# Docker Network Commands

## Overview
Docker networking allows containers to communicate with each other and with the outside world. Below are some common Docker network commands along with their purposes, descriptions, and examples.

## Commands

### 1. `docker network ls`
- **Purpose**: List all networks.
- **Description**: Displays a list of all networks created in Docker.
- **Example**:
    ```sh
    docker network ls
    ```

### 2. `docker network create`
- **Purpose**: Create a new network.
- **Description**: Creates a user-defined network that containers can be attached to.
- **Example**:
    ```sh
    docker network create my_network
    ```

### 3. `docker network inspect`
- **Purpose**: Display detailed information about a network.
- **Description**: Provides detailed information about a specific network, including its configuration and connected containers.
- **Example**:
    ```sh
    docker network inspect my_network
    ```

### 4. `docker network connect`
- **Purpose**: Connect a container to a network.
- **Description**: Connects a running container to a specified network.
- **Example**:
    ```sh
    docker network connect my_network my_container
    ```

### 5. `docker network disconnect`
- **Purpose**: Disconnect a container from a network.
- **Description**: Disconnects a running container from a specified network.
- **Example**:
    ```sh
    docker network disconnect my_network my_container
    ```

### 6. `docker network rm`
- **Purpose**: Remove one or more networks.
- **Description**: Deletes one or more networks by name or ID.
- **Example**:
    ```sh
    docker network rm my_network
    ```

## Conclusion
These commands help manage Docker networks, allowing for better container communication and network organization. Use these commands to create, inspect, connect, disconnect, and remove Docker networks as needed.