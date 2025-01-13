## Lab 07: Using Environment Variables

**Description:** Configure services dynamically using environment variables.

**Objective:** Pass configuration parameters via `.env` files or Compose.

### Example:
```yaml
version: '3.9'
services:
  app:
    image: myapp:latest
    environment:
      - APP_ENV=production
```
```bash
# Start with environment variables
docker-compose up -d

# Inspect environment variables
docker inspect <container_name>
```

**Architecture:**
- Externalize configuration using environment variables.

---