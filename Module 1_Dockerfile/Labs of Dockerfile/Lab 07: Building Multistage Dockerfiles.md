### **Lab 07: Building Multistage Dockerfiles**
- **Title:** Create a Multi-Stage Build  
- **Description:** Use multiple `FROM` instructions to optimize image size and separate build steps.  
- **Purpose:** Reduce image size by excluding unnecessary build dependencies.  
- **Key Concepts:**  
  - **Multi-Stage Build**: Combines multiple `FROM` stages in a Dockerfile.

**Example:**
```Dockerfile
# Build stage
FROM golang:1.20 as builder
WORKDIR /app
COPY . .
RUN go build -o main .

# Final stage
FROM alpine:latest
COPY --from=builder /app/main /app/main
CMD ["/app/main"]
```