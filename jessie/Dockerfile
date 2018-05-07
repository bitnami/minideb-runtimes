FROM bitnami/minideb@sha256:d1ff68fd9f227e8b7b17d5c53c187024384e38698427163e7fd6cc099d1894c1
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=jessie-r19
