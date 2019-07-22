FROM bitnami/minideb@sha256:ce241ca19d61254bc07ab8a757e82f01e214c5cd1a3ce27530c91fff887ea4a0
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=jessie-r424
