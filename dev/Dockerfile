# About Image: Use LTS version for maintenance purpose and use alpine to reduce image size.
FROM node:10-alpine

LABEL vendor="Dynamic Lab"
LABEL maintainer="pangxiaoxi@gmail.com, cndream@gmail.com"
LABEL description="dv-web dev docker image"

ARG DEV_HOME

WORKDIR $DEV_HOME

# Install build dependencies
RUN apk update \
    && apk add --no-cache build-base libpng-dev bash

# run npm install at CMD level, so that we don't need to build new images again and again
CMD cd app && \
    npm install --quiet &&\
    npm start
