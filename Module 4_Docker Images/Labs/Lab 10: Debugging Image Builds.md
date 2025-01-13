## Lab 10: Debugging Image Builds

**Description:** Troubleshoot common issues during Docker builds.

**Objective:** Learn to debug Dockerfile errors.

### Example:
```dockerfile
# Dockerfile
FROM ubuntu:latest
RUN apt-get update && apt-get install -y non-existent-package
```
```bash
# Build the image to see the error
docker build -t debug-demo .
```

**Architecture:**
- Use `docker build` logs and intermediate containers for debugging.

---

These labs provide a comprehensive journey from understanding Docker images to advanced optimization techniques. Let me know if you need further refinements or additional details!
