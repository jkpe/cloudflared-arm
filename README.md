# cloudflared-arm

The official cloudflared docker repo does not provide an arm image. https://hub.docker.com/r/cloudflare/cloudflared

This repo builds a docker image of 'cloudflared' that can be used with a Raspberry Pi.

https://hub.docker.com/r/jkpe/cloudflared

```
  cloudflared:
    container_name: cloudflared
    image: jkpe/cloudflared:latest
    volumes:
      - ./cloudflared:/etc/cloudflared
    entrypoint:
      - cloudflared
    command:
      - tunnel
      - run
    restart: always
```
