FROM alpine:latest

RUN \
    apt -y update && \
    # apt -y dist-upgrade && \
    # apt -y install build-essential yasm nasm p7zip-full && \
    # apt -y clean && \
    # git config --global user.email "builder@localhost" && \
    # git config --global user.name "Builder" && \
    # git config --global advice.detachedHead false

ENV CARGO_HOME="/opt/cargo" RUSTUP_HOME="/opt/rustup" PATH="/opt/cargo/bin:${PATH}"
RUN curl https://sh.rustup.rs -sSf | bash -s -- -y --no-modify-path && \
    cargo install cargo-c && rm -rf "${CARGO_HOME}"/registry "${CARGO_HOME}"/git

RUN --mount=src=.,dst=/input \
    for s in /input/*.sh; do cp $s /usr/bin/$(echo $s | sed -e 's|.*/||' -e 's/\.sh$//'); done
