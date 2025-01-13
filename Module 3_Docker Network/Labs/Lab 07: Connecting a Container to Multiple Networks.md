## Lab 07: Connecting a Container to Multiple Networks

**Description:** Attach a container to multiple networks for flexible communication.  
**Objective:** Explore scenarios where a container requires connections to different networks.  

### Example:
```bash
# Create two networks
docker network create network1
docker network create network2

# Run a container and attach it to both networks
docker run -dit --name multi_network_container --network network1 busybox

docker network connect network2 multi_network_container

# Inspect the container's network settings
docker network inspect network1
```

**Architecture:** A container connected to two distinct networks.  
**Outcome:** Learn to manage containers on multiple networks.
