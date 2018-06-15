FROM ubuntu:18.04
MAINTAINER citra
RUN mkdir -p /tmp/pkgs
COPY install_package.py /tmp/pkgs
RUN apt-get update && apt-get install -y build-essential wget git python-launchpadlib ccache
RUN cd /tmp/pkgs && python2 install_package.py \
    libsdl2-dev 2.0.7+dfsg1-3ubuntu1 bionic          \
    qtbase5-dev 5.9.3+dfsg-0ubuntu2 bionic           \
    qttools5-dev-tools 5.9.5-0ubuntu1 bionic         \
    libqt5opengl5-dev 5.9.3+dfsg-0ubuntu2 bionic     \
    qt5-qmltooling-plugins 5.9.3-0ubuntu1 bionic     \
    qtdeclarative5-dev 5.9.3-0ubuntu1 bionic         \
    qtmultimedia5-dev 5.9.3-0ubuntu3 bionic          \
    libicu57 57.1-6ubuntu0.2 bionic                  \
    cmake 3.10.2-1ubuntu2 bionic
RUN rm -rf /tmp/pkgs
