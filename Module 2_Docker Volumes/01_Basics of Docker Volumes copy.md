### **Basics of Docker Volumes**
- Volumes are used to persist data beyond the lifecycle of a container.
- They can be shared between multiple containers.
- Volumes are stored in a part of the host filesystem managed by Docker (`/var/lib/docker/volumes/`).

### **Types of Volumes**
1. **Named Volumes:**
    - Explicitly created and managed by the user.
    - Can be reused by specifying their name.
    
    **Command Example:**
    ```bash
    docker volume create my_named_volume
    docker run -v my_named_volume:/app/data my_image
    ```

2. **Anonymous Volumes:**
    - Created and managed by Docker.
    - Cannot be easily reused as they do not have a specific name.
    
    **Command Example:**
    ```bash
    docker run -v /app/data my_image
    ```

3. **Host Volumes:**
    - Map a specific directory on the host to a directory in the container.
    - Useful for sharing data between the host and the container.
    
    **Command Example:**
    ```bash
    docker run -v /path/on/host:/app/data my_image
    ```