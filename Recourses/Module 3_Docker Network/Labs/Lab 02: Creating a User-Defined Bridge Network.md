## Lab 02: Creating a User-Defined Bridge Network

**Description:** Learn to create and manage a user-defined bridge network.  
**Objective:** Explore custom bridge networks for better isolation and control.  

### Example:
```bash
# Create a new bridge network
docker network create my_bridge_network

# Run a container attached to the custom network
docker run -dit --name my_container --network my_bridge_network busybox

# Inspect the network
docker network inspect my_bridge_network
```

**Architecture:** One container connected to a user-defined bridge network.  
**Outcome:** Understand the benefits of using custom bridge networks.
