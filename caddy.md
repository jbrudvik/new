# New [Caddy](https://caddyserver.com/docs/) server

### Start hard-coded server

- On port 80: `$ sudo caddy respond "hello" --listen :80`
  - Replying with a status code: `$ sudo caddy 418 --listen :80`
- On non-privileged port: `$ caddy respond "hello" --listen :8080`

### Start file server

- On port 80: `$ sudo caddy file-server --listen :80`
  - Serving specified directory: `$ sudo caddy file-server --root directory --listen :80`
  - With file browser: `$ sudo caddy file-server --browse --listen :80`
- On non-privileged port: `$ caddy file-server --listen :8080`
- On domain over HTTPS: `$ sudo caddy file-server --domain example.com`

### Start reverse proxy

- On port 80: `$ sudo caddy reverse-proxy --from :80 --to :8080`
- On non-privileged port: `$ caddy reverse-proxy --from :8080 --to :8081`
- On domain over HTTPS: `$ caddy reverse-proxy --from example.com --to :8081`

### Start server with [Caddyfile](https://caddyserver.com/docs/caddyfile-tutorial)

- Start: `$ sudo caddy start`
- Reload: `$ caddy reload`
- Stop: `$ caddy stop`
