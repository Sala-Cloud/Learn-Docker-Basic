### **Lab 8: Managing Volumes**
- **Title:** Persistent Data in Containers  
- **Description:** Use the `VOLUME` instruction to define persistent storage areas in your Docker container.  
- **Purpose:** Ensure data is not lost when the container is stopped or removed.  
- **Key Concepts:**  
  - **VOLUME**: Declares a mount point for data persistence.

**Example:**
```Dockerfile
# Base image
FROM alpine:latest

# Declare a volume
VOLUME ["/data"]

CMD ["sh"]
```