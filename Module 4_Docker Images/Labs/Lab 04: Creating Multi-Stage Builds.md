## Lab 04: Creating Multi-Stage Builds

**Description:** Use multi-stage builds to optimize image size.

**Objective:** Learn to separate build and runtime environments.

### Example:
```dockerfile
# Dockerfile
FROM golang:1.20 AS builder
WORKDIR /app
COPY main.go .
RUN go build -o app

FROM alpine:latest
COPY --from=builder /app/app /app
CMD ["/app"]
```
```bash
# Build the image
docker build -t my-go-app .

# Run the image
docker run --rm my-go-app
```

**Architecture:**
- First stage: Compile the application.
- Second stage: Include only the compiled binary.

---
