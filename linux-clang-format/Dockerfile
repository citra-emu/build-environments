FROM ubuntu:18.04
LABEL maintainer="citraemu"
RUN useradd -m -s /bin/bash citra
RUN apt-get update && apt-get -y full-upgrade
RUN apt-get install -y git clang-format-6.0
USER citra
