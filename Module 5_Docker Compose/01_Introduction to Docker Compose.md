# Introduction to Docker Compose

Docker Compose is a tool that allows you to define and manage multi-container Docker applications. With Docker Compose, you can use a YAML file to configure your application's services, networks, and volumes, making it easier to manage and deploy complex applications.

## Key Features of Docker Compose

- **Multi-Container Deployment**: Define and run multiple containers as a single service.
- **Service Definition**: Use a `docker-compose.yml` file to configure your application's services.
- **Networking**: Automatically create and manage networks for your containers.
- **Volume Management**: Easily manage data volumes for persistent storage.
- **Environment Configuration**: Use environment variables to configure your services.

Docker Compose simplifies the process of setting up and running multi-container Docker applications, making it an essential tool for developers and DevOps engineers.

## Basic Example

Here is a simple example of a `docker-compose.yml` file:

```yaml
version: '3'
services:
    web:
        image: nginx
        ports:
            - "80:80"
    db:
        image: mysql
        environment:
            MYSQL_ROOT_PASSWORD: example
```

In this example, we define two services: `web` and `db`. The `web` service uses the Nginx image and maps port 80 on the host to port 80 on the container. The `db` service uses the MySQL image and sets an environment variable for the MySQL root password.

To start the application, simply run:

```sh
docker-compose up
```

This command will start both the `web` and `db` services as defined in the `docker-compose.yml` file.

Docker Compose is a powerful tool that can help you manage and deploy your Docker applications with ease.