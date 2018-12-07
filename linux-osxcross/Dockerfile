FROM ubuntu:18.04
MAINTAINER citra
RUN useradd -m -s /bin/bash citra
RUN apt-get update && apt-get -y full-upgrade
RUN apt-get install -y make cmake ccache clang xz-utils wget p7zip-full git qt5-default qttools5-dev-tools
COPY osxcross-setup.sh /tmp/
RUN bash -e /tmp/osxcross-setup.sh
ENV PATH="${PATH}:/opt/osxcross/bin/"
COPY toolchain.cmake /opt/osxcross/
