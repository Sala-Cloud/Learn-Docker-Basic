### **Lab 10: Customizing Image Labels**
- **Title:** Adding Metadata with Labels  
- **Description:** Use the `LABEL` instruction to include metadata about your Docker image.  
- **Purpose:** Add documentation or management information to your image.  
- **Key Concepts:**  
  - **LABEL**: Adds key-value pairs as metadata.

**Example:**
```Dockerfile
# Base image
FROM ubuntu:20.04

# Add metadata
LABEL maintainer="example@example.com" \
      version="1.0" \
      description="This is an example image."

CMD ["echo", "Dockerfile with labels"]
