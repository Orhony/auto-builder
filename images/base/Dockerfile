FROM alpine:latest

RUN \
    apt -y update && \
    apt -y dist-upgrade && \
    apt -y install build-essential yasm nasm p7zip-full && \
    apt -y clean
