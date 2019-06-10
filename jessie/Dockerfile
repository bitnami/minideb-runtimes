FROM bitnami/minideb@sha256:b32d71ddf1c57316f30948f1e9a40f9c323d72e4cc22459fb0a0eb5b1e4c57ef
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=jessie-r385
