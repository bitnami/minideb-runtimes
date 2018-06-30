FROM bitnami/minideb@sha256:57e3aa9eeff315deba56773b8f6c526d1f0b18435035e1f9efda1ee0bcee198e
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=stretch-r10
