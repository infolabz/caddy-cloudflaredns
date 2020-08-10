# caddy-cloudflaredns

Enable DNS challenge by adding  caddy tls directive in Caddyfile
```code
       tls {
           dns cloudflare {env.CLOUDFLARE_API_TOKEN}
       }
```
## docker-compose example
```code
    version: "3.7"
    services:
      caddy:
        image: infolabsdev/caddy-cloudflaredns:latest
        restart: on-failure
        environment:
          CLOUDFLARE_API_TOKEN: token
          CLOUDFLARE_EMAIL: email
          ACME_AGREE: 'true'
```