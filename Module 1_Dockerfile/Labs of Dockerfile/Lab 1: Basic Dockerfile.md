### **Lab 1: Basic Dockerfile**
- **Title:** Writing Your First Dockerfile  
- **Description:** Create a simple Dockerfile that builds an image with a base OS and a custom message.  
- **Purpose:** Understand the basic structure of a Dockerfile and the `FROM` and `CMD` instructions.  
- **Key Concepts:**  
  - **FROM**: Specifies the base image.  
  - **CMD**: Defines the default command to run when the container starts.  

**Example:**
```Dockerfile
# Use an official Ubuntu as the base image
FROM ubuntu:20.04

# Default command to display a message
CMD ["echo", "Hello, Docker!"]
```