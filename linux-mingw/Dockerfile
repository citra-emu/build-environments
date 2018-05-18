FROM ubuntu:18.04
MAINTAINER citra
RUN apt-get update && apt-get install -y gpg wget git python3-pip ccache g++-mingw-w64-x86-64 gcc-mingw-w64-x86-64 mingw-w64-tools cmake
COPY errno.h /usr/x86_64-w64-mingw32/include/
# HACK: the repository does not contain necessary packages for 18.04, we'll use packages for 17.10 for now
RUN echo 'deb http://ppa.launchpad.net/tobydox/mingw-w64/ubuntu artful main ' > /etc/apt/sources.list.d/extras.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv '72931B477E22FEFD47F8DECE02FE5F12ADDE29B2' && apt-get update
RUN apt-get install -y sdl2-mingw-w64 qt5base-mingw-w64 qt5tools-mingw-w64 libsamplerate-mingw-w64 qt5multimedia-mingw-w64
