### **Lab 06: Using ENTRYPOINT**
- **Title:** Defining the Entry Point for Your Container  
- **Description:** Explore the difference between `ENTRYPOINT` and `CMD` by defining a custom entry point for your container.  
- **Purpose:** Configure the container to behave like an executable.  
- **Key Concepts:**  
  - **ENTRYPOINT**: Sets the main process of the container.

**Example:**
```Dockerfile
# Base image
FROM alpine:latest

# Define entry point
ENTRYPOINT ["echo"]

# Provide default arguments
CMD ["This is the default message"]
```