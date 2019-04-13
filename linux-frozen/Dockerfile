FROM ubuntu:18.04
LABEL maintainer="citraemu"
RUN useradd -m -s /bin/bash citra && mkdir -p /tmp/pkgs
COPY install_package.py /tmp/pkgs
RUN apt-get update && apt-get install -y build-essential wget git python-launchpadlib ccache ninja-build
RUN cd /tmp/pkgs && python2 install_package.py \
    libsdl2-dev 2.0.7+dfsg1-3ubuntu1 bionic          \
    qtbase5-dev 5.9.3+dfsg-0ubuntu2 bionic           \
    libqt5opengl5-dev 5.9.3+dfsg-0ubuntu2 bionic     \
    qt5-qmltooling-plugins 5.9.3-0ubuntu1 bionic     \
    qtdeclarative5-dev 5.9.3-0ubuntu1 bionic         \
    qtmultimedia5-dev 5.9.3-0ubuntu3 bionic          \
    libicu57 57.1-6ubuntu0.2 bionic                  \
    cmake 3.10.2-1ubuntu2 bionic                     \
    libavcodec-dev 7:3.4.4-0ubuntu0.18.04.1 bionic   \
    libavformat-dev 7:3.4.4-0ubuntu0.18.04.1 bionic  \
    libswscale-dev 7:3.4.4-0ubuntu0.18.04.1 bionic
RUN rm -rf /tmp/pkgs
USER citra
