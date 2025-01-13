## Lab 04: Using Host Network

**Description:** Understand how to use the host network to bypass Docker's network abstraction.  
**Objective:** Learn the implications of using the host network.  

### Example:
```bash
# Run a container using the host network
docker run -dit --name host_network_test --network host busybox

# Verify that the container shares the host's network namespace
docker exec host_network_test ip addr
```

**Architecture:** A container using the host's network stack.  
**Outcome:** Learn about use cases and limitations of the host network.
