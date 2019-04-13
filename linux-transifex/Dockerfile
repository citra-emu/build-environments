FROM alpine
LABEL maintainer="citraemu"
RUN adduser -u 1000 -D -s /bin/bash citra
RUN apk update && apk add build-base cmake python3-dev qt5-qttools-dev qt5-qtmultimedia-dev
RUN pip3 install transifex-client
USER citra
