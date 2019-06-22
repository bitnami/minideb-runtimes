FROM bitnami/minideb@sha256:1d02dc3053adf3a06ad604c0998d0c4ec0ff34348abae71d923e4c3089e9f557
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libssl1.0.2 libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=stretch-r313
