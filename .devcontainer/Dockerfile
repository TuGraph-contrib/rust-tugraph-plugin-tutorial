FROM antkiller996/rust-tugraph:latest

ARG USERNAME=root
ARG USER_UID=1000
ARG USER_GID=$USER_UID


RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -G sudo -m $USERNAME -s /bin/bash \
    && apt-get update \
    && apt-get install -y sudo \
    && echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER $USERNAME