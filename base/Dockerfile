#syntax=docker/dockerfile-upstream:1.4.0-rc1
FROM archlinux

WORKDIR /tmp

RUN mkdir -p /etc/pacman.d/hooks
COPY clean_pacman_cache.hook /etc/pacman.d/hooks/

RUN pacman -Syu base-devel unzip --noconfirm
