## Lab 09: Health Checks

**Description:** Implement health checks for service monitoring.

**Objective:** Ensure services are healthy before starting dependencies.

### Example:
```yaml
version: '3.9'
services:
  web:
    image: nginx:latest
    healthcheck:
      test: ["CMD", "curl", "-f", "http://localhost"]
      interval: 30s
      timeout: 10s
      retries: 3
```
```bash
# Start with health checks
docker-compose up -d
```

**Architecture:**
- Monitor and manage service health proactively.

---