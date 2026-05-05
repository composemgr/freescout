## 👋 Welcome to freescout 🚀

Self-hosted freescout application

## 📋 Description

Self-hosted freescout application

## 🚀 Services

- **freescout**: tiredofit/freescout:latest

### Infrastructure Components

- **freescout-db**: Mariadb database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/freescout/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/freescout" ~/.local/srv/docker/freescout
cd ~/.local/srv/docker/freescout
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install freescout
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:8090

## 📂 Volumes

- `./volumes/data/freescout` - Data storage
- `./volumes/config/freescout` - Data storage
- `./volumes/data/db/mariadb/freescout` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f freescout
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
