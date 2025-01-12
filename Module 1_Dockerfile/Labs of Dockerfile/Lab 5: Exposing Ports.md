### **Lab 5: Exposing Ports**
- **Title:** Configuring Networking for Containers  
- **Description:** Use the `EXPOSE` instruction to specify the ports your container will listen on.  
- **Purpose:** Inform users about network ports that should be mapped.  
- **Key Concepts:**  
  - **EXPOSE**: Documents the ports a container listens to.

**Example:**
```Dockerfile
# Use Nginx as the base image
FROM nginx:latest

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
```