## Lab 09: Building Minimal Images

**Description:** Create lightweight images by reducing unnecessary layers.

**Objective:** Optimize image size for better performance.

### Example:
```dockerfile
# Dockerfile
FROM alpine:latest
RUN apk add --no-cache curl
CMD ["curl", "--version"]
```
```bash
# Build and check image size
docker build -t minimal-curl .
docker images minimal-curl
```

**Architecture:**
- Use smaller base images like `alpine`.

---