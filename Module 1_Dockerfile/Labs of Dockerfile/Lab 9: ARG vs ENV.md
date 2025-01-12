### **Lab 9: ARG vs ENV**
- **Title:** Build-Time vs Runtime Variables  
- **Description:** Learn the difference between `ARG` and `ENV` by creating a Dockerfile with configurable build-time and runtime variables.  
- **Purpose:** Understand when to use build arguments and environment variables.  
- **Key Concepts:**  
  - **ARG**: Defines build-time variables.  
  - **ENV**: Defines runtime variables.

**Example:**
```Dockerfile
# Base image
FROM alpine:latest

# Build-time argument
ARG APP_VERSION=1.0.0

# Runtime environment variable
ENV APP_ENV=production

# Display both variables
CMD ["sh", "-c", "echo Version: $APP_VERSION, Environment: $APP_ENV"]
```