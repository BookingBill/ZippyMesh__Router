# Docker Registry Distribution

The ZippyMesh LLM Router is available on multiple registries for resilience and convenience.

## Available Registries

### Docker Hub (Primary)
```bash
docker pull zippymesh/router:v0.1.0-alpha
```

### GitHub Container Registry
```bash
docker pull ghcr.io/zippymesh/router:v0.1.0-alpha
```

### Quay.io
```bash
docker pull quay.io/zippymesh/router:v0.1.0-alpha
```

## Running with Docker Compose

Create a `docker-compose.yml` file:

```yaml
version: '3.8'
services:
  zippymesh:
    image: zippymesh/router:v0.1.0-alpha
    ports:
      - "127.0.0.1:20128:20128"
    environment:
      ZIPPY_PORT: 20128
    restart: unless-stopped
```

Then start the service:
```bash
docker-compose up -d
```

## Health Check
Verify the installation:
```bash
curl http://localhost:20128/api/health
```
