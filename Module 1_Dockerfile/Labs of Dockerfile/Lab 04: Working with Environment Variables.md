### **Lab 04: Working with Environment Variables**
- **Title:** Setting Environment Variables  
- **Description:** Use the `ENV` instruction to set environment variables in your Dockerfile.  
- **Purpose:** Pass configuration settings to the container at runtime.  
- **Key Concepts:**  
  - **ENV**: Defines an environment variable accessible during build and runtime.

**Example:**
```Dockerfile
# Base image
FROM ubuntu:20.04

# Set an environment variable
ENV APP_ENV=production

# Use the variable in the command
CMD ["echo", "The environment is $APP_ENV"]
```