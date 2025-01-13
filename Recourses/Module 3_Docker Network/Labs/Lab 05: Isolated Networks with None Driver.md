## Lab 05: Isolated Networks with None Driver

**Description:** Explore the none network driver to create isolated containers.  
**Objective:** Understand the isolation provided by the none driver.  

### Example:
```bash
# Run a container with the none network driver
docker run -dit --name isolated_container --network none busybox

# Verify that the container has no network access
docker exec isolated_container ping -c 3 google.com
```

**Architecture:** A container isolated from any network.  
**Outcome:** Understand the use cases for network isolation.
