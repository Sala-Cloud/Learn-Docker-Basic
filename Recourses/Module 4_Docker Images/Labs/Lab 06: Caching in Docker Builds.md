## Lab 06: Caching in Docker Builds

**Description:** Understand Docker build cache and how to leverage it.

**Objective:** Speed up builds by reusing unchanged layers.

### Example:
```dockerfile
# Dockerfile
FROM ubuntu:latest
RUN apt-get update && apt-get install -y curl
RUN echo "Caching Demo"
```
```bash
# Build the image twice to see caching in action
docker build -t caching-demo .
docker build -t caching-demo .
```

**Architecture:**
- Docker reuses layers that haven’t changed.

---