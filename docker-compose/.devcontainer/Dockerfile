ARG VARIANT="jammy"

FROM ubuntu:${VARIANT}

ARG USERNAME=vscode
ARG USER_GID=1000
ARG USER_UID=1000

RUN apt-get update && \
    apt-get -y upgrade --no-install-recommends && \
    apt-get -y install --no-install-recommends \
    zsh \
    git \
    && rm -rf /var/lib/apt/lists/* && \
    groupadd --gid $USER_GID $USERNAME && \
    useradd -s /bin/zsh --uid $USER_UID --gid $USERNAME -m $USERNAME