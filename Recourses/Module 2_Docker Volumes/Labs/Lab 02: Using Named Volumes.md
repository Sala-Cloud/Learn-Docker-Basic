## Lab 02: Using Named Volumes

**Description:** Use named volumes to persist data in a container.  
**Objective:** Understand how to specify and reuse named volumes.  

### Example:
```bash
# Run a container with a named volume
docker run -d --name volume_demo -v my_named_volume:/data busybox sleep 1000

# Inspect the volume
docker volume inspect my_named_volume
```

**Outcome:** You will know how to use and inspect named volumes.
