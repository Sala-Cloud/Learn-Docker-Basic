## Lab 02: Creating a Basic Docker Image

**Description:** Build a simple Docker image using a Dockerfile.

**Objective:** Learn how to write a Dockerfile and build an image.

### Example:
```dockerfile
# Dockerfile
FROM alpine:latest
RUN apk add --no-cache curl
CMD ["curl", "--version"]
```
```bash
# Build the Docker image
docker build -t my-curl-image .

# Run a container using the image
docker run --rm my-curl-image
```

**Architecture:**
- Base image (`FROM alpine:latest`).
- Additional layers for each `RUN` instruction.

---
