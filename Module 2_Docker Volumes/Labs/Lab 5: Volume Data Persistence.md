## Lab 5: Volume Data Persistence

**Description:** Use volumes to persist data beyond the container lifecycle.  
**Objective:** Retain data even after containers are removed.  

### Example:
```bash
# Start a container
docker run -d --name persist_test -v my_data:/data busybox sleep 1000

# Write data to the volume
docker exec persist_test sh -c 'echo "Persistent Data" > /data/file.txt'

# Remove the container and verify the data
docker run --rm -v my_data:/data busybox cat /data/file.txt
```

**Outcome:** You will understand data persistence with Docker volumes.
