# s6 on Ubuntu Bionic
FROM markusma/ubuntu:bionic

# set version for s6 overlay
ARG OVERLAY_VERSION="v2.0.0.1"
ARG OVERLAY_ARCH="amd64"

RUN curl -o /tmp/s6-overlay.tar.gz -L "https://github.com/just-containers/s6-overlay/releases/download/${OVERLAY_VERSION}/s6-overlay-${OVERLAY_ARCH}.tar.gz" \
 && tar xfz /tmp/s6-overlay.tar.gz -C / \
 && rm -rf /tmp/*

# keep all env variables
ENV S6_KEEP_ENV=1

ENTRYPOINT [ "/init"  ]
