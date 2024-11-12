FROM mcr.microsoft.com/devcontainers/rust:latest

# Prevent interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Update and install essential packages
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    git \
    llvm \
    clang \
    libelf-dev \
    iproute2 \
    bpftool \
    pkg-config \
    libssl-dev \
    make \
    sudo \
    unzip \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Install Aya CLI
RUN cargo install bindgen-cli

# Switch to the non-root user
USER vscode
