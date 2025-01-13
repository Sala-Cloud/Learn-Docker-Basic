## Lab 10: Securing Docker Networks

**Description:** Implement best practices for securing Docker networks.  
**Objective:** Learn to restrict and secure network traffic between containers.  

### Example:
```bash
# Create a network with a custom subnet and gateway
docker network create --subnet=192.168.1.0/24 secure_network

# Run a container on the secure network
docker run -dit --name secure_container --network secure_network busybox

# Verify the network configuration
docker network inspect secure_network
```

**Architecture:** A container connected to a restricted and secure network.  
**Outcome:** Understand how to secure container networks effectively.

---

These labs are designed to provide a comprehensive learning experience for Docker networking, from the basics to advanced topics. Let me know if additional details are required!
