# Contributing

This is a docker image of an enhanced version of n8n.

## Add an extra node

You can add an extra node to the image by editing the [Dockerfile](./images/neon8n-debian/Dockerfile), add the following
line:

```shell
RUN cd /usr/lib/node_modules/n8n && npm install n8n-nodes-${NODE_NAME}
```
