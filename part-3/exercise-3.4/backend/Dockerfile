FROM node:10-alpine

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/backend-example-docker.git /app && \
    cd /app && npm install && \
    apk del git && \
    chown -R node /app

WORKDIR /app

USER node

EXPOSE 8000
CMD ["npm", "start"]
