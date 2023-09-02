FROM archlinux:latest
RUN pacman -Syu \
    pacman -S \
        make \
        unzip \
        curl \
        wget \
        # Software required to use the AUR
        base-devel \
        git \
    # Install packwiz from AUR
    && git clone https://aur.archlinux.org/packwiz-git.git \
    && cd packwiz-git \
    && makepkg \
    && ls | pacman -U
ENV SHELL=/bin/bash \