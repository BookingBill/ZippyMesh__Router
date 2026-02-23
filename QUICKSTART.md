# Quick Start — 5 Minutes

## Docker (Easiest)

1. Install Docker (https://docker.com/download)

2. Create `docker-compose.yml`:
```yaml
version: '3.8'
services:
  zippymesh:
    image: zippymesh/router:v0.1.0-alpha
    ports:
      - "127.0.0.1:20128:20128"
    environment:
      ZIPPY_PORT: 20128
```

3. Start:
```bash
docker-compose up -d
```

4. Test:
```bash
curl http://localhost:20128/api/health
```

## Using It

```bash
curl http://localhost:20128/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-4o",  # or any Ollama model
    "messages": [{"role": "user", "content": "Say hello"}]
  }'
```

## Need Help?

- [Full Documentation](https://github.com/BookingBill/ZippyMesh__Router/wiki)
- [Troubleshooting](docs/troubleshooting.md)
- [GitHub Issues](https://github.com/BookingBill/ZippyMesh__Router/issues)

That's it! 🎉
