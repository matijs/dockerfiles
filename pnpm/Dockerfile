FROM node:20.8.1-alpine

LABEL org.opencontainers.image.authors matijs <matijs@gmail.com>
LABEL org.opencontainers.image.source https://github.com/matijs/dockerfiles/blob/main/pnpm/Dockerfile

RUN apk add --no-cache git
RUN corepack enable
RUN corepack prepare pnpm@latest --activate

ENTRYPOINT [ "docker-entrypoint.sh" ]

CMD [ "node" ]

