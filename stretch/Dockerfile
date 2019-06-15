FROM bitnami/minideb@sha256:c23ed09d3fe3087d7c3434c900d3bd440d8c4eee5abbfaf489d5831e20a1e63b
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libssl1.0.2 libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=stretch-r306
