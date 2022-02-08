FROM rust:slim
# FROM rust:1.58.1-slim

RUN apt update \
    && apt install -y --no-install-recommends \
    apt-utils \
    git \
    ca-certificates \
    procps \
    && apt autoremove -y \
    && apt clean -y \
    && rm -rf /var/lib/apt/lists/* \
    && rustup component add rustfmt \
    && cargo install cargo-watch
