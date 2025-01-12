## Lab 04: Bind Mounts Basics

**Description:** Use bind mounts to link a host directory to a container.  
**Objective:** Learn to synchronize changes between host and container.  

### Example:
```bash
# Run a container with a bind mount
docker run -d -v $(pwd):/app busybox sleep 1000

# Verify synchronization by modifying files in $(pwd)
```

**Outcome:** You will understand how to set up and use bind mounts.
