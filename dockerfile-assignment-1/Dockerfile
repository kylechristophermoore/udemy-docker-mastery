# use this empty Dockerfile to build your assignment

# NOTE: The instructions are now in the README.md file in this directory.
FROM node:6-alpine

RUN apk add --no-cache tini

COPY package.json package.json

WORKDIR /usr/src/app

RUN npm install \
    && npm cache clean --force

EXPOSE 3000

COPY . .

CMD ["/sbin/tini", "--node", "./bin/www"]