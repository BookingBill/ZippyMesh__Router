# Installation Guide

## Option 1: Docker (Recommended)
```bash
docker pull zippymesh/router:v0.1.0-alpha
docker-compose up -d
```

## Option 2: Standalone Binary
1. Download from [Releases](https://github.com/BookingBill/ZippyMesh__Router/releases)
2. Verify with SHA256SUMS
3. Run: `./zippymesh-router-linux-x64`

## Option 3: npm
```bash
npm install -g zippymesh-router
zippymesh-router
```

## Option 4: Kubernetes
```bash
helm install zippymesh zippymesh/router  # coming v0.2.0
```
