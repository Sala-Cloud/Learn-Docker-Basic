## Lab 01: Understanding Docker Images

**Description:** Learn the basics of Docker images, including their purpose and structure.

**Objective:** Understand how Docker images are used as the foundation for running containers.

### Example:
```bash
# Pull an official Docker image
docker pull ubuntu:latest

# List downloaded images
docker images

# Inspect the image details
docker inspect ubuntu:latest
```

**Architecture:**
- Docker images consist of multiple layers built on top of each other.
- Each layer represents a set of changes to the filesystem.
---