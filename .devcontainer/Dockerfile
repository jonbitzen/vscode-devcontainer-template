

FROM ubuntu:24.04

ARG USERNAME=ubuntu

RUN apt-get update && \
    apt-get install -y \
    sudo \
    git \
    git-lfs \
    build-essential \
    cmake

RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
    chmod 0440 /etc/sudoers.d/$USERNAME

RUN usermod -a -G video ubuntu

USER ${USERNAME}
