# Juara MT

Landing dos domínios `portaljuara.com.br` e `juaramt.com.br` — página estática sobre Juara/MT.

## Stack

- HTML estático + CSS inline (sem build step)
- Servido por Nginx em container

## Rodar local

```bash
# abrir direto no navegador
xdg-open index.html

# ou via docker
docker build -t juara-mt .
docker run --rm -p 8080:80 juara-mt
# → http://localhost:8080
```

## Deploy (Easypanel)

- App tipo **App** → Source: GitHub → Build: **Dockerfile** (raiz)
- Porta: `80`
- Domínios: `juaramt.com.br` e `portaljuara.com.br` apontando pro mesmo serviço
