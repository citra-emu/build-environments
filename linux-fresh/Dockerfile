FROM ubuntu:18.04
LABEL maintainer="citraemu"
RUN useradd -m -s /bin/bash citra
RUN apt-get update && apt-get -y full-upgrade
RUN apt-get install -y p7zip-full build-essential libsdl2-dev qtbase5-dev libqt5opengl5-dev qtmultimedia5-dev qttools5-dev qttools5-dev-tools libavcodec-dev libavformat-dev libswscale-dev wget git ccache cmake ninja-build
USER citra
