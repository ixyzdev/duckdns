```markdown
<p align="center">
  <img src="https://raw.githubusercontent.com/homarr-labs/dashboard-icons/main/png/duckdns.png" alt="DuckDNS Logo" width="160">
</p>

# DuckDNS (linuxserver.io) – Actualización de IP con Docker

Servicio para mantener actualizado un subdominio `*.duckdns.org` con la IP pública del host usando la imagen `lscr.io/linuxserver/duckdns`.

## Estructura

```
.
├─ docker-compose.yml
└─ .env
```

## Requisitos

- Cuenta y subdominio en DuckDNS.
- Token de API.
- Docker y Docker Compose.

## Configuración

Presente en el archivo `.env.example`

```bash
TZ=America/Santiago

SUBDOMAINS=tu-subdominio
TOKEN=token

LOG_FILE=true
PUID=1000
PGID=1000
```
## Puesta en marcha

```bash
docker compose up -d
docker logs -f duckdns
```



