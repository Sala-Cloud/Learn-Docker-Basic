**Lab 02: Adding Files to the Container**

- **Title:** Adding Files to the Container  
- **Description:** Learn to add files to your Docker container using the `COPY` and `ADD` instructions.  
- **Purpose:** Understand how to include necessary files in your Docker image for your application to function correctly.  
- **Key Concepts:**  
    - **COPY**: Copies files or directories from the build context to the image.  
    - **ADD**: Similar to `COPY`, but can also handle remote files or archives.

**Example:**
```Dockerfile
# Use a lightweight base image
FROM alpine:latest

# Copy local file into the container
COPY index.html /usr/share/nginx/html/index.html