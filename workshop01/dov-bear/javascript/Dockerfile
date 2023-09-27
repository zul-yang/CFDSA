FROM node:20

ARG APP_PORT=3000
ARG NAME="myapp"
ARG HASH="myapphash"

LABEL name=${NAME}

ARG APP_DIR=/app
WORKDIR ${APP_DIR}

COPY main.js .
COPY package.json .
COPY package-lock.json .
COPY public public
COPY views views

RUN npm ci

ENV PORT=${APP_PORT}
EXPOSE ${PORT}

ENTRYPOINT [ "node", "main.js" ]