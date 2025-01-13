## Lab 05: Building Images with Compose

**Description:** Use Compose to build Docker images from a Dockerfile.

**Objective:** Automate the image build process within Compose.

### Example:
```yaml
version: '3.9'
services:
  app:
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "5000:5000"
```
```dockerfile
# Dockerfile
FROM python:3.9
COPY app.py /app.py
CMD ["python", "app.py"]
```
```bash
# Build and run
docker-compose up --build
```

**Architecture:**
- Automate custom image builds for applications.

---