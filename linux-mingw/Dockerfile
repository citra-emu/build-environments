FROM ubuntu:18.04
LABEL maintainer="citraemu"
RUN useradd -m -s /bin/bash citra && mkdir -p /tmp/pkgs
RUN apt-get update && apt-get install -y gpg wget git python3-pip ccache p7zip-full g++-mingw-w64-x86-64 gcc-mingw-w64-x86-64 mingw-w64-tools cmake ninja-build
# workaround broken headers in Ubuntu MinGW package
COPY errno.h /usr/x86_64-w64-mingw32/include/
# add mingw-w64 auxiliary ppa repository
RUN echo 'deb http://ppa.launchpad.net/tobydox/mingw-w64/ubuntu bionic main ' > /etc/apt/sources.list.d/extras.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv '72931B477E22FEFD47F8DECE02FE5F12ADDE29B2' && apt-get update
RUN apt-get install -y sdl2-mingw-w64 qt5base-mingw-w64 qt5tools-mingw-w64 libsamplerate-mingw-w64 qt5multimedia-mingw-w64
COPY mingw-setup.sh /tmp/pkgs
RUN cd /tmp/pkgs && bash -e mingw-setup.sh
USER citra
