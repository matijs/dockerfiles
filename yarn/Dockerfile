FROM node:20.12.1-alpine3.19

LABEL org.opencontainers.image.authors matijs <matijs@gmail.com>
LABEL org.opencontainers.image.source https://github.com/matijs/dockerfiles/blob/main/yarn/Dockerfile

RUN apk add --no-cache git
RUN npm install --global npm@latest
RUN npm cache clean --force
RUN corepack enable
RUN yarn set version stable

ENTRYPOINT [ "docker-entrypoint.sh" ]

CMD [ "node" ]

