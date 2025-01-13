# Docker Troubleshooting Labs

## Overview
Docker troubleshooting involves identifying and resolving issues within the Docker ecosystem, such as container errors, image building issues, networking problems, and daemon failures. This document includes detailed labs to help you understand and troubleshoot Docker effectively.

---

## Lab 1: Checking Docker Service Status

**Description:** Learn to verify if the Docker Engine service is running properly.

**Objective:** Understand how to start, stop, and check the status of the Docker service.

### Example:
```bash
# Check Docker service status
systemctl status docker

# Start the Docker service
systemctl start docker

# Enable Docker to start on boot
systemctl enable docker
```

**Key Points:**
- The Docker service (`dockerd`) must be running for container operations.
- Issues often arise when the service fails to start due to configuration errors.

---

## Lab 2: Analyzing Docker Logs

**Description:** Use Docker logs to diagnose issues with containers or the daemon.

**Objective:** Learn to access and interpret Docker logs for debugging purposes.

### Example:
```bash
# View Docker daemon logs
journalctl -u docker

# Check logs for a specific container
docker logs <container_id>

# Stream container logs in real time
docker logs -f <container_id>
```

**Key Points:**
- Logs provide detailed insights into runtime and error messages.
- Use `docker logs` to view application-level logs for containers.

---

## Lab 3: Resolving Container Networking Issues

**Description:** Diagnose and resolve networking issues with Docker containers.

**Objective:** Understand how to inspect and troubleshoot Docker networks.

### Example:
```bash
# List all Docker networks
docker network ls

# Inspect a specific network
docker network inspect <network_name>

# Reconnect a container to a network
docker network connect <network_name> <container_id>
```

**Key Points:**
- Misconfigured networks often lead to communication failures between containers.
- Use `docker network inspect` to debug network configurations.

---

## Lab 4: Managing Disk Space for Docker

**Description:** Learn how to free up disk space used by Docker resources.

**Objective:** Understand how to remove unused images, containers, and volumes.

### Example:
```bash
# Remove all stopped containers
docker container prune

# Remove unused volumes
docker volume prune

# Remove dangling images
docker image prune

# Remove all unused Docker resources
docker system prune -a
```

**Key Points:**
- Over time, Docker can consume significant disk space.
- Regular cleanup prevents performance degradation.

---

## Lab 5: Restarting Docker Containers on Failure

**Description:** Configure containers to restart automatically on failure.

**Objective:** Ensure high availability by using restart policies.

### Example:
```bash
# Run a container with a restart policy
docker run -d --restart=on-failure:3 nginx

# Check the restart count
docker inspect -f '{{ .RestartCount }}' <container_id>
```

**Key Points:**
- Restart policies improve container resilience during failures.

---

## Lab 6: Debugging Docker Build Errors

**Description:** Identify and fix errors encountered during Docker image builds.

**Objective:** Use build logs and intermediate containers for debugging.

### Example:
```bash
# Build an image and display verbose logs
docker build -t debug-demo .

# View intermediate containers created during the build
docker ps -a
```

**Key Points:**
- Errors during builds often stem from incorrect Dockerfile instructions.
- Analyze build logs to identify the specific failing step.

---

## Lab 7: Troubleshooting Container Resource Constraints

**Description:** Monitor and adjust resource limits for containers.

**Objective:** Resolve performance issues caused by insufficient resources.

### Example:
```bash
# Run a container with resource limits
docker run -d --memory=512m --cpus=1 nginx

# Monitor container resource usage
docker stats
```

**Key Points:**
- Containers can be constrained using memory and CPU limits.
- `docker stats` provides real-time resource usage data.

---

## Lab 8: Resolving Image Pull Issues

**Description:** Troubleshoot problems while pulling images from a registry.

**Objective:** Identify and fix network or authentication-related issues.

### Example:
```bash
# Check Docker daemon logs for errors
journalctl -u docker

# Pull an image with authentication
docker login

docker pull myregistry.com/myimage:latest
```

**Key Points:**
- Image pull issues often result from registry authentication or network problems.

---

## Lab 9: Debugging Stuck or Unresponsive Containers

**Description:** Diagnose and recover from unresponsive containers.

**Objective:** Learn to use `docker exec` and `docker kill` commands.

### Example:
```bash
# Access the container's shell
docker exec -it <container_id> /bin/bash

# Force-stop an unresponsive container
docker kill <container_id>
```

**Key Points:**
- Unresponsive containers can be investigated using `docker exec`.
- Use `docker kill` to terminate containers in critical situations.

---

## Lab 10: Diagnosing Docker Daemon Startup Issues

**Description:** Troubleshoot Docker daemon startup problems.

**Objective:** Learn to identify and fix configuration or compatibility issues.

### Example:
```bash
# Check Docker daemon configuration
cat /etc/docker/daemon.json

# Test Docker daemon startup manually
dockerd --debug
```

**Key Points:**
- Startup issues are often related to incorrect configurations in `daemon.json`.
- The `--debug` flag provides additional insights into daemon behavior.

---

This comprehensive set of labs provides practical troubleshooting steps for Docker. Each lab focuses on a specific area, offering examples and key points to build your expertise.
