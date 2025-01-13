## Lab 07: Using Private Registries

**Description:** Push and pull images from a private Docker registry.

**Objective:** Learn to work with private registries.

### Example:
```bash
# Run a private Docker registry
docker run -d -p 5000:5000 --name registry registry:2

# Tag and push the image
docker tag my-curl-image localhost:5000/my-curl-image

docker push localhost:5000/my-curl-image

# Pull the image
docker pull localhost:5000/my-curl-image
```

**Architecture:**
- Local Docker registry serves as a private image store.

---
