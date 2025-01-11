## Dockerfile Labs Instructions and Meaning

### Instructions for Students

1. **Clone the Repository**: Start by cloning the repository to your local machine using the command:
    ```sh
    git clone <repository-url>
    ```

2. **Navigate to the Lab Directory**: Change your directory to the lab folder where the Dockerfile is located:
    ```sh
    cd /path/to/Labs-of-Dockerfile
    ```

3. **Review the Dockerfile**: Open the Dockerfile in your preferred text editor and review its contents to understand the instructions and configurations.

4. **Build the Docker Image**: Use the Dockerfile to build a Docker image by running:
    ```sh
    docker build -t <image-name> .
    ```

5. **Run the Docker Container**: Once the image is built, run a container using the image:
    ```sh
    docker run -d --name <container-name> <image-name>
    ```

6. **Verify the Container**: Check if the container is running correctly by using:
    ```sh
    docker ps
    ```

7. **Experiment and Modify**: Feel free to experiment by modifying the Dockerfile and rebuilding the image to see how changes affect the container.

### Example Dockerfile

Here is an example Dockerfile that you can use for your lab:

```dockerfile
FROM ubuntu:20.04
WORKDIR /app
COPY . .
RUN apt-get update && apt-get install -y python3 python3-pip
RUN pip3 install -r requirements.txt
EXPOSE 5000
CMD ["python3", "app.py"]
```

### Meaning of Dockerfile Labs

The Dockerfile labs are designed to provide hands-on experience with creating and managing Docker containers. By working through these labs, students will learn how to:

- Write and understand Dockerfiles.
- Build Docker images from Dockerfiles.
- Run and manage Docker containers.
- Experiment with different configurations and optimizations in Dockerfiles.

These labs aim to equip students with practical skills in containerization, which is essential for modern software development and deployment.
