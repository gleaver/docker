FROM base/devel:latest
MAINTAINER Guy Leaver <guy@guyleaver.co.uk>

RUN useradd -ms /bin/bash lal -G wheel && \
    echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

# Update repos
RUN pacman --noconfirm --noprogress -Syu

# Basic toolchain
RUN pacman --noconfirm --noprogress -Sq \
  clang llvm cmake extra-cmake-modules gtest

# Allegro
RUN pacman --noconfirm --noprogress -Sq allegro

VOLUME ["/home/lal/volume"]
