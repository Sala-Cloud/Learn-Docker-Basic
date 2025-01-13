## Lab 08: Compose Override Files

**Description:** Use override files to adjust configurations for specific environments.

**Objective:** Dynamically customize service behavior.

### Example:
```yaml
# docker-compose.override.yml
version: '3.9'
services:
  app:
    ports:
      - "3000:3000"
```
```bash
# Start with override file
docker-compose -f docker-compose.yml -f docker-compose.override.yml up
```

**Architecture:**
- Use multiple configuration files for environment-specific settings.

---