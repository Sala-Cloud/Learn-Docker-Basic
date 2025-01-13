## Lab 04: Configuring Networks in Compose

**Description:** Create custom networks for isolating services.

**Objective:** Understand how to define and manage networks in Compose.

### Example:
```yaml
version: '3.9'
services:
  web:
    image: nginx:latest
    networks:
      - frontend
  db:
    image: postgres:latest
    networks:
      - backend
networks:
  frontend:
  backend:
```
```bash
# Start the services
docker-compose up -d

# Inspect networks
docker network ls
```

**Architecture:**
- Segregate services into different networks for security and performance.

---