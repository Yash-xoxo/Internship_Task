FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

# Install VLC and audio/video dependencies
RUN apt update && apt install -y \
    vlc pulseaudio dbus-x11 x11-utils sudo && \
    useradd -m dockeruser && \
    echo "dockeruser ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# Switch to non-root user
USER dockeruser

# Default command
CMD ["vlc"]
