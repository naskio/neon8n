# neon8n

Docker image of an enhanced version of n8n.

![n8n](https://github.com/naskio/neon8n/raw/main/assets/n8n-logo.png)

[GitHub repository](https://github.com/naskio/neon8n)

[Docker Hub](https://hub.docker.com/r/naskio/neon8n/)

[![Docker Pulls](https://img.shields.io/docker/pulls/naskio/neon8n.svg?style=for-the-badge)](https://hub.docker.com/r/naskio/neon8n)

## Extra features

- *Python 3.10* included by default.
- `Python Function` node: run python snippets on n8n.
- `Has Changed` node: check if the results of the current execution is different from the previous one.
- `InfluxDB` node: write/read data to/from InfluxDB v2+ using the Flux Language.

## Example

Docker Compose file:

```yaml
version: '3.8'

services:
  neon8n:
    image: naskio/neon8n:latest
    restart: always
    container_name: neon8n
    environment:
      GENERIC_TIMEZONE: ${TIMEZONE}
      TZ: ${TIMEZONE}
    ports:
      - "5678:5678"
    volumes:
      - data:/home/node/.n8n

volumes:
  data:
```

-----------------------------------------------------

# Acknowledgements

Based on [n8n-python](https://github.com/naskio/docker-n8n-python)

# Contribute

Contributions are welcome! Please open an issue or pull request if you have any suggestions.

See the [contributing guide](./CONTRIBUTING.md) for more information.

# License

[GNU GENERAL PUBLIC LICENSE v3](./LICENSE)
