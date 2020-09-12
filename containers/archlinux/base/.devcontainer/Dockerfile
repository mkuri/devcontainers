FROM archlinux:latest

# Install needed packages and setup non-root user. Use a separate RUN statement to add your own dependencies.
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID
COPY library-scripts/*.sh /tmp/library-scripts/
RUN pacman -Syu --noconfirm \
    && /bin/bash /tmp/library-scripts/common-arch.sh "${USERNAME}" "${USER_UID}" "${USER_GID}" \
    && rm -rf /var/cache/pacman/pkg/*

# Install base packages
RUN pacman -Syu --noconfirm git neovim \
    && rm -rf /var/cache/pacman/pkg/*