# Advanced Dockerfile Techniques

## Introduction
In this lab, you will learn how to create a more advanced Dockerfile. This Dockerfile will include additional instructions to optimize the image and handle environment variables.

## Purpose
The purpose of this lab is to teach you how to create a more advanced Dockerfile that includes optimization techniques and the use of environment variables. By the end of this lab, you will be able to create efficient and manageable Docker images using multi-stage builds.

## Objectives
- Understand how to use environment variables in a Dockerfile.
- Learn how to optimize Docker images.
- Create a multi-stage build Dockerfile.

## Steps

### Step 1: Create a Dockerfile
Create a new file named `Dockerfile` in your project directory.

### Step 2: Define the Base Image
Use the official Node.js image as the base image.

```dockerfile
FROM node:14 AS build
```

### Step 3: Set the Working Directory
Set the working directory inside the container.

```dockerfile
WORKDIR /app
```

### Step 4: Copy Files
Copy the application files from your local machine to the container.

```dockerfile
COPY package*.json ./
```

### Step 5: Install Dependencies
Install the application dependencies.

```dockerfile
RUN npm install
```

### Step 6: Copy the Rest of the Application Files
Copy the rest of the application files to the container.

```dockerfile
COPY . .
```

### Step 7: Build the Application
Build the application.

```dockerfile
RUN npm run build
```

### Step 8: Define the Production Image
Define the production image using a multi-stage build to reduce the final image size.

```dockerfile
FROM node:14-alpine AS production
WORKDIR /app
COPY --from=build /app .
```

### Step 9: Set Environment Variables
Set environment variables using the `ENV` instruction.

```dockerfile
ENV NODE_ENV=production
```

### Step 10: Specify the Command to Run
Specify the command to run when the container starts.

```dockerfile
CMD ["node", "dist/app.js"]
```

## Building the Docker Image
To build the Docker image from the Dockerfile, use the following command:

```sh
docker build -t my-node-app:prod .
```

## Running the Docker Container
To run the Docker container from the image you just built, use the following command:

```sh
docker run -p 3000:3000 my-node-app:prod
```

## Conclusion
In this lab, you learned how to create a more advanced Dockerfile, use environment variables, and optimize Docker images using multi-stage builds. These techniques will help you create more efficient and manageable Docker images.

## Additional Resources
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)
- [Best Practices for Writing Dockerfiles](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- [Multi-stage Builds](https://docs.docker.com/develop/develop-images/multistage-build/)