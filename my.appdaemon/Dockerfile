# Base on official Home Assistant Community Add-on base
FROM ghcr.io/hassio-addons/appdaemon:stable

# Set shell to bash for better error handling during build
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN \
    apk add --no-cache py3-ruamel.yaml \
    && pip3 install --no-cache-dir --upgrade \
        pymodbus \
        spotipy

LABEL maintainer="jougs"
LABEL description="AppDaemon with pymodbus, ruamel.yaml, and spotipy"
