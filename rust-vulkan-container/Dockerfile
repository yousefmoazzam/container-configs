ARG RUST_VERSION="1.78.0"

FROM rust:${RUST_VERSION}-slim

ENV NVIDIA_DRIVER_CAPABILITIES=all
ENV NVIDIA_VISIBLE_DEVICES=all

COPY ./nvidia_icd.json /usr/share/vulkan/icd.d/

RUN apt-get update && \
    apt-get install -y build-essential git python3.11 cmake libvulkan-dev vulkan-tools mesa-utils libxcursor-dev libxrandr-dev libxi-dev && \
    apt-get clean
