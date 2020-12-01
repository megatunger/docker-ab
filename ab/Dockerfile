FROM alpine

ENV TERM linux
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "nano"]
RUN apk --no-cache add apache2-utils parallel
