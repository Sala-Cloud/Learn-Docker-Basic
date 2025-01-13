# Docker Compose Command Line

Docker Compose is a tool for defining and running multi-container Docker applications. Here are some common Docker Compose commands with descriptions and examples:

## `docker-compose up`
Starts the services defined in the `docker-compose.yml` file.

**Example:**
```sh
docker-compose up
```

## `docker-compose down`
Stops and removes the containers, networks, and volumes created by `docker-compose up`.

**Example:**
```sh
docker-compose down
```

## `docker-compose build`
Builds or rebuilds the services defined in the `docker-compose.yml` file.

**Example:**
```sh
docker-compose build
```

## `docker-compose pull`
Pulls the latest version of the images defined in the `docker-compose.yml` file.

**Example:**
```sh
docker-compose pull
```

## `docker-compose start`
Starts the existing containers for a service.

**Example:**
```sh
docker-compose start
```

## `docker-compose stop`
Stops the running containers without removing them.

**Example:**
```sh
docker-compose stop
```

## `docker-compose restart`
Restarts the running containers.

**Example:**
```sh
docker-compose restart
```

## `docker-compose logs`
Displays the logs from the running containers.

**Example:**
```sh
docker-compose logs
```

## `docker-compose ps`
Lists the containers that are part of the application.

**Example:**
```sh
docker-compose ps
```

## `docker-compose exec`
Executes a command in a running container.

**Example:**
```sh
docker-compose exec <service_name> <command>
```
**Example:**
```sh
docker-compose exec web bash
```

## `docker-compose config`
Validates and views the Compose file.

**Example:**
```sh
docker-compose config
```

## `docker-compose version`
Displays the Docker Compose version information.

**Example:**
```sh
docker-compose version
```

## `docker-compose run`
Runs a one-time command against a service.

**Example:**
```sh
docker-compose run <service_name> <command>
```
**Example:**
```sh
docker-compose run web python manage.py migrate
```

## `docker-compose rm`
Removes stopped service containers.

**Example:**
```sh
docker-compose rm
```

## `docker-compose scale`
Sets the number of containers to run for a service.

**Example:**
```sh
docker-compose scale <service_name>=<number>
```
**Example:**
```sh
docker-compose scale web=3
```
