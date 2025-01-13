## Lab 06: Scaling Services

**Description:** Learn to scale services with Compose.

**Objective:** Run multiple instances of a service to handle increased load.

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
# Scale the service
docker-compose up -d --scale web=3

# Verify scaled services
docker-compose ps
```

**Architecture:**
- Scale horizontally by running multiple container instances.

---