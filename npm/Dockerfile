FROM node:20.18.1-alpine3.20

LABEL org.opencontainers.image.authors="matijs <matijs@gmail.com>"
LABEL org.opencontainers.image.source="https://github.com/matijs/dockerfiles/blob/main/npm/Dockerfile"

RUN apk add --no-cache git
RUN npm install --global npm@latest
RUN npm cache clean --force

ENTRYPOINT [ "docker-entrypoint.sh" ]

CMD [ "node" ]

