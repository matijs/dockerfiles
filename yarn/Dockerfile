FROM node:20.9.0-alpine

LABEL org.opencontainers.image.authors matijs <matijs@gmail.com>
LABEL org.opencontainers.image.source https://github.com/matijs/dockerfiles/blob/main/yarn/Dockerfile

RUN apk add --no-cache git
RUN corepack enable
RUN yarn set version stable

ENTRYPOINT [ "docker-entrypoint.sh" ]

CMD [ "node" ]

