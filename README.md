# Lisgar-LLM-IThink

## Render deployment

This repository can be deployed on Render using the `render.yaml` manifest.

It defines:
- `open-notebook-proxy`: public NGINX web service routing UI and API traffic
- `open-notebook`: private Open Notebook backend service
- `surrealdb`: private SurrealDB service

### Deploy steps

1. Push this repository to GitHub.
2. Create a Render account and connect the repository.
3. Render should detect `render.yaml` and create the services.
4. Update `OPEN_NOTEBOOK_ENCRYPTION_KEY` in Render secrets for production.

### Notes

- `nginx.render.conf` is the proxy config used by Render.
- Keep local `docker-compose.yml` for local development.
