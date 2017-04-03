FROM alpine:3.2

RUN \
    apk --update add \
    nodejs unrar bash git curl ca-certificates && \
    rm -f /var/cache/apk/* && \
    echo "Packages successfully installed"

RUN mkdir -p /app

ADD app/package.json /app

WORKDIR /app

RUN npm install nodemon -g

RUN npm install

ADD app /app

CMD [ "npm", "start" ]