FROM alpine:latest

RUN \
    apk -U upgrade && \
    apk -y install yasm p7zip && \
    git config --global user.email "builder@localhost" && \
    git config --global user.name "Builder" && \
    git config --global advice.detachedHead false
