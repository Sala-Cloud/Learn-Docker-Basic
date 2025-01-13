## Lab 03: Using Volumes in Compose

**Description:** Use volumes to persist data across container restarts.

**Objective:** Learn to configure persistent storage with Compose.

### Example:
```yaml
version: '3.9'
services:
  db:
    image: postgres:latest
    volumes:
      - db_data:/var/lib/postgresql/data
volumes:
  db_data:
```
```bash
# Start the service
docker-compose up -d

# Check volume usage
docker volume inspect <volume_name>
```

**Architecture:**
- Use named volumes for persistent storage.

---
