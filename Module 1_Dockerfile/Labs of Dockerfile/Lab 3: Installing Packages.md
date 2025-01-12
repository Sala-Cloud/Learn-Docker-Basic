### **Lab 3: Installing Packages**
- **Title:** Install Software in the Image  
- **Description:** Create a Dockerfile that installs software packages like `curl` or `wget` during the image build.  
- **Purpose:** Automate the installation of required tools for your container.  
- **Key Concepts:**  
  - **RUN**: Executes commands during the build process.

**Example:**
```Dockerfile
# Start with Ubuntu
FROM ubuntu:20.04

# Update package manager and install curl
RUN apt-get update && apt-get install -y curl

# Default command
CMD ["curl", "--version"]
```