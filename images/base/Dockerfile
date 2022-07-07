FROM alpine:latest

RUN \
    apk -U upgrade && \
    apk add yasm p7zip git && \
    git config --global user.email "builder@localhost" && \
    git config --global user.name "Builder" && \
    git config --global advice.detachedHead false