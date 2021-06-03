FROM rust:1.52.1-slim

RUN apt update \
    && apt install -y --no-install-recommends \
    apt-utils \
    git \
    ca-certificates \
    procps \
    && apt autoremove -y \
    && apt clean -y \
    && rm -rf /var/lib/apt/lists/* \
    && rustup component add rustfmt --toolchain 1.52.1-x86_64-unknown-linux-gnu \
    && cargo install cargo-watch
