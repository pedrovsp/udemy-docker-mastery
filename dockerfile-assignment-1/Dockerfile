FROM node:alpine

EXPOSE 3000

RUN apk add --update tini

RUN mkdir -p /usr/src/app

COPY . /usr/src/app

WORKDIR /usr/src/app

RUN npm install && npm cache clean --force

CMD [ "/sbin/tini", "--", "node", "./bin/www" ]
