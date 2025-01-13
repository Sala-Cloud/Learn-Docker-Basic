## Lab 03: Communication Between Containers in a Custom Network

**Description:** Enable communication between multiple containers on the same network.  
**Objective:** Understand how containers on the same network communicate.  

### Example:
```bash
# Create a custom network
docker network create app_network

# Run two containers on the custom network
docker run -dit --name container1 --network app_network busybox

docker run -dit --name container2 --network app_network busybox

# Test communication between the containers
docker exec container1 ping -c 3 container2
```

**Architecture:** Two containers communicating over a shared network.  
**Outcome:** Learn how containers communicate within the same network.
