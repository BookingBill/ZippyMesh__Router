# ZippyMesh LLM Router — Alpha v0.1.0

⚠️ **ALPHA NOTICE**: Unstable API, expect changes until v1.0.0

## What is ZippyMesh?

ZippyMesh is a **self-healing edge computing mesh network** powered by ZippyCoin.

This is the **LLM Router** — the first dApp. It routes AI model requests to the cheapest/fastest provider:
- Local Ollama models (Qwen, Llama, DeepSeek)
- Cloud providers (Claude, GPT-4o, Gemini via ZippyMesh Marketplace)
- Fallback chains automatically handle provider failures

## Quick Start (5 minutes)

```bash
docker-compose up -d
curl http://localhost:20128/api/health
```

Send an LLM request:
```bash
curl http://localhost:20128/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-4o",
    "messages": [{"role": "user", "content": "Hello"}]
  }'
```

## Features

✅ **Multi-provider routing** — Ollama + cloud in one interface
✅ **Cost optimization** — Automatically use cheapest provider
✅ **Failure handling** — Fallback chains ensure availability
✅ **OpenAI-compatible** — Works with any LLM client
✅ **ZippyCoin integration** — Pay for cloud routes with ZippyCoin
✅ **Privacy-first** — Self-host locally, control all data

## Deployment Options

- **Docker** (recommended) — `docker-compose up`
- **Standalone binary** — Download & run
- **npm** — `npm install -g zippymesh-router`
- **Kubernetes** — Helm chart (coming soon)

## What's Coming Next?

- **Q2 2026**: dVPN (Mysterium alternative)
- **Q3 2026**: Decentralized Storage (IPFS alternative)
- **Q4 2026**: Compute Marketplace
- **2027**: Global CDN + Game Server Clustering

## Support

- 📖 [Documentation](docs/)
- 🐛 [Report Bugs](https://github.com/BookingBill/ZippyMesh__Router/issues)
- 💬 [Ask Questions](https://github.com/BookingBill/ZippyMesh__Router/discussions)
- 💰 [ZippyCoin Integration](docs/ZIPPYCOIN.md)

## Security

Localhost-only by default. For external access:
- Use reverse proxy (nginx, traefik) + TLS
- Or SSH tunnel / VPN access
- See [SECURITY.md](docs/SECURITY.md) for patterns

## License

Apache 2.0
