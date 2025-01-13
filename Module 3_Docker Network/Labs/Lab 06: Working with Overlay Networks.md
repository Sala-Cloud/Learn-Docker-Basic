## Lab 06: Working with Overlay Networks

**Description:** Set up an overlay network for container communication across multiple hosts.  
**Objective:** Learn how to enable multi-host networking.  

### Example:
```bash
# Initialize Docker Swarm
docker swarm init

# Create an overlay network
docker network create -d overlay my_overlay_network

# Deploy a service to the overlay network
docker service create --name my_service --network my_overlay_network busybox sleep 1000
```

**Architecture:** A distributed network spanning multiple Docker hosts.  
**Outcome:** Understand overlay networks and their role in Swarm mode.
