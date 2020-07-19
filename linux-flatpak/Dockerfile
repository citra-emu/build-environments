FROM ubuntu:20.04
LABEL maintainer="citraemu"
RUN apt-get update && apt-get -y full-upgrade
RUN apt-get install -y p7zip-full wget git flatpak flatpak-builder ca-certificates sshfs curl fuse dnsutils gnupg2 sudo
RUN flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
RUN flatpak install -y flathub org.kde.Platform//5.13 org.kde.Sdk//5.13
