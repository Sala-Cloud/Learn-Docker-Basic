## Lab 01: Introduction to Docker Compose

**Description:** Learn the basics of Docker Compose and how it simplifies managing multi-container applications.

**Objective:** Understand the purpose of Docker Compose and create a basic `docker-compose.yml` file.

### Example:
```yaml
version: '3.9'
services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
```
```bash
# Start the services
docker-compose up -d

# List running services
docker-compose ps
```

**Architecture:**
- Multi-container management using a single YAML configuration file.
- Simple definition of services and networks.

---