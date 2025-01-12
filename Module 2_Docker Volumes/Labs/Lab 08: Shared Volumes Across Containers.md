## Lab 08: Shared Volumes Across Containers

**Description:** Share a volume between multiple containers.  
**Objective:** Learn how to manage shared data.  

### Example:
```bash
# Start two containers with the same volume
docker run -d --name container1 -v shared_volume:/data busybox sleep 1000
docker run -d --name container2 -v shared_volume:/data busybox sleep 1000

# Write data in one container and read it in the other
docker exec container1 sh -c 'echo "Shared Data" > /data/shared.txt'
docker exec container2 cat /data/shared.txt
```

**Outcome:** You will understand how to share volumes between containers.
