FROM node:22.15.1-alpine3.21

LABEL org.opencontainers.image.authors="matijs <matijs@gmail.com>"
LABEL org.opencontainers.image.source="https://github.com/matijs/dockerfiles/blob/main/nodejs/Dockerfile"

RUN apk add --no-cache git
RUN npm install --global npm@latest
RUN npm cache clean --force
RUN corepack enable
RUN corepack prepare pnpm@latest --activate
RUN pnpm config set store-dir ~/.local/share/pnpm/store

ENTRYPOINT [ "docker-entrypoint.sh" ]

CMD [ "node" ]

