## Lab 08: DNS Resolution in Docker Networks

**Description:** Understand how Docker handles DNS resolution for containers.  
**Objective:** Explore how containers resolve names to communicate.  

### Example:
```bash
# Create a custom network
docker network create dns_test_network

# Run two containers with names
docker run -dit --name dns_container1 --network dns_test_network busybox

docker run -dit --name dns_container2 --network dns_test_network busybox

# Test DNS resolution
docker exec dns_container1 ping -c 3 dns_container2
```

**Architecture:** Containers using Docker's built-in DNS server.  
**Outcome:** Understand Docker's DNS capabilities.