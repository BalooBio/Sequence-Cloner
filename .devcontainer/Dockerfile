FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    build-essential \
    clang \
    gcc \
    g++ \
    make \
    python3 \
    python3-pip \
    curl \
    git \
    unzip \
    wget \
    valgrind \
    vim \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install check50 style50 submit50

RUN useradd -m vscode && echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER vscode
WORKDIR /home/vscode
