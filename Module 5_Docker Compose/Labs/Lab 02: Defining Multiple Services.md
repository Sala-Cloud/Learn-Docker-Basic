## Lab 02: Defining Multiple Services

**Description:** Configure multiple services in a single Compose file.

**Objective:** Learn to define interconnected services in one configuration.

### Example:
```yaml
version: '3.9'
services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
  app:
    image: python:3.9
    command: python -m http.server 8000
    ports:
      - "8000:8000"
```
```bash
# Start the services
docker-compose up -d

# Access services on ports 8080 and 8000
```

**Architecture:**
- Define and run multiple containers in parallel.
- Link services for easy intercommunication.

---
