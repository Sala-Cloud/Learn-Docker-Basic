## Lab 03: Using Anonymous Volumes

**Description:** Learn to work with anonymous volumes and explore their lifecycle.  
**Objective:** Differentiate between named and anonymous volumes.  

### Example:
```bash
# Run a container with an anonymous volume
docker run -d -v /data busybox sleep 1000

# List the created volume
docker volume ls
```

**Outcome:** Understand anonymous volume usage and lifecycle.
