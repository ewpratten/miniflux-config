# miniflux-config
Configuration for my personal Miniflux server

The following must be set in `.env`:

```text
POSTGRES_PASSWORD=...
TUNNEL_TOKEN=...
```

On setup, migrations and users must be handled:

```sh
docker compose run miniflux /usr/bin/miniflux -migrate
docker compose run miniflux /usr/bin/miniflux -create-admin
```

**Note:** Cloudflare Access must look for the service at `http://miniflux:8080`