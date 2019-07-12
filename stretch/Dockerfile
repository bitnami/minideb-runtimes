FROM bitnami/minideb@sha256:ab5d138dbc17726e14a665e553f76ea07b502bce43a9932844222e9ac27c126e
LABEL maintainer "Bitnami <containers@bitnami.com>"

RUN install_packages libssl-dev libssl1.0.2 libsqlite3-dev

# The following security actions are recommended by some security scans.
# https://console.bluemix.net/docs/services/va/va_index.html
RUN  sed -i 's/^PASS_MAX_DAYS.*/PASS_MAX_DAYS    90/' /etc/login.defs && \
  sed -i 's/^PASS_MIN_DAYS.*/PASS_MIN_DAYS    0/' /etc/login.defs && \
  sed -i 's/sha512/sha512 minlen=8/' /etc/pam.d/common-password

ENV BITNAMI_IMAGE_VERSION=stretch-r330
