FROM bitnami/minideb@sha256:988d72968f5ffc5762977afb061d764987cc07c28ee22dad5f1d6fbf54cbd486
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libssl1.0.2 libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=stretch-r265
