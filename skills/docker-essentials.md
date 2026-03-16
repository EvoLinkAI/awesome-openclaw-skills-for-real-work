# Docker Essentials

> Full Docker and Docker Compose command reference — containers, images, volumes, networks, and debugging, all in one skill.

**ClawHub:** https://clawhub.ai/Arnarsson/docker-essentials · ⭐ 21 · 196 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

Docker Essentials gives your agent a comprehensive Docker reference covering the complete container lifecycle. From running a container to debugging inside it, managing multi-service stacks with Compose, cleaning up disk space, and building multi-stage production images — it's all here.

Essential for developers who use Docker daily and want their agent to help without requiring a manual lookup every time.

## How to Install

```bash
clawhub install docker-essentials
```

## Key Capabilities

- Container lifecycle — run, stop, start, restart, remove
- Log streaming and inspection (`docker logs -f`, `docker inspect`, `docker stats`)
- Shell access inside running containers (`docker exec -it`)
- Image building — Dockerfile, build args, multi-stage builds, no-cache
- Docker Compose — up, down, scale, rebuild, per-service logs
- Networking — create, connect, disconnect, inspect
- Volumes — create, mount, prune
- System cleanup — `docker system prune`, `docker image prune -a`
- File copy in/out of containers (`docker cp`)

## Usage Examples

**Spin up a Postgres database:**
```bash
docker run -d \
  --name postgres \
  -e POSTGRES_PASSWORD=secret \
  -e POSTGRES_DB=mydb \
  -v postgres-data:/var/lib/postgresql/data \
  -p 5432:5432 \
  postgres:15
```

**Development container with live code mount:**
```bash
docker run -it --rm \
  -v $(pwd):/app \
  -w /app \
  -p 3000:3000 \
  node:18 \
  npm run dev
```

**Debug inside a running container:**
```bash
docker exec -it container_name bash
docker logs -f container_name         # Stream logs
docker stats container_name           # CPU/memory live
docker cp container_name:/app/log.txt ./local/  # Extract file
```

**Multi-stage build (small production image):**
```dockerfile
FROM node:18 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
```

**Full cleanup:**
```bash
docker system prune -a --volumes   # Remove everything unused
docker system df                   # Check disk usage first
```

## Requirements

- **Binaries:** `docker` (and `docker-compose` for Compose workflows)
- **API Keys:** None
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Use `--rm` for one-off containers — they clean up automatically on exit
- Never embed real passwords in `docker run -e` in scripts — use `.env` files or secrets management
- `docker system prune -a` removes ALL unused images, not just dangling ones — check `docker system df` first
- Add `.dockerignore` to your projects — it drastically speeds up builds
- Combine `RUN` statements in Dockerfiles to reduce image layers
- `docker-compose up -d --build` is the fastest way to rebuild and restart a changed service

## Related Skills

- [Git Essentials](./git-essentials.md) — Version control alongside your container workflow
- [Tmux](./tmux.md) — Keep long-running `docker-compose up` sessions persistent
- [n8n Workflow Automation](./n8n-workflow-automation.md) — Automate deployment pipelines
- [Security Auditor](./security-auditor.md) — Audit Dockerfiles and container configs for vulnerabilities
