# A dns update client for Dynu

Use with:

```bash
docker run -d --restart=always --name ddns \
  -e DYN_HOSTNAME="${DYN_HOSTNAME}" \
  -e DYN_USER="${DYN_USER}" \
  -e DYN_PASS="${DYN_PASS}" \
  ghcr.io/snyssen/dynu-docker-client:1.0
```

or with docker-compose:

```yaml
version: "3"

services:
  ddns:
    container_name: ddns
    image: ghcr.io/snyssen/dynu-docker-client:1.0
    environment:
      - DYN_HOSTNAME=${DYN_HOSTNAME}
      - DYN_USER=${DYN_USER}
      - DYN_PASS=${DYN_PASS}
    restart: always
```
