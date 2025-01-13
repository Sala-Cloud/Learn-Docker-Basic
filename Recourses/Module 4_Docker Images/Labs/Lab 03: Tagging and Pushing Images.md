## Lab 03: Tagging and Pushing Images

**Description:** Tag your Docker image and push it to a Docker registry.

**Objective:** Understand how to manage and share images.

### Example:
```bash
# Tag the image
docker tag my-curl-image myusername/my-curl-image:1.0

# Push the image to Docker Hub
docker push myusername/my-curl-image:1.0
```

**Architecture:**
- Image is identified by its repository, name, and tag.

---