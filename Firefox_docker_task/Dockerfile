FROM ubuntu:22.04

# Install dependencies
RUN apt-get update && apt-get install -y \
    firefox \
    x11-apps \
    libx11-xcb1 \
    libxtst6 \
    libgtk-3-0 \
    libdbus-glib-1-2 \
    libasound2 \
    && apt-get clean

# Set display variable for GUI
ENV DISPLAY=:0
