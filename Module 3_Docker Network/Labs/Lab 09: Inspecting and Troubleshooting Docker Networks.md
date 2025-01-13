## Lab 09: Inspecting and Troubleshooting Docker Networks

**Description:** Learn to inspect and troubleshoot Docker networks.  
**Objective:** Use Docker commands to identify and resolve network issues.  

### Example:
```bash
# Inspect a network
docker network inspect bridge

# Troubleshoot container connectivity
docker exec container1 ping -c 3 8.8.8.8

# Remove an unused network
docker network prune
```

**Architecture:** A container network with diagnostic steps.  
**Outcome:** Gain proficiency in network inspection and troubleshooting.
