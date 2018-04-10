[![CircleCI](https://circleci.com/gh/bitnami/minideb-runtimes/tree/master.svg?style=shield)](https://circleci.com/gh/bitnami/minideb-runtimes/tree/master)

# `bitnami/minideb-runtimes`

## TL;DR

```dockerfile
FROM bitnami/minideb-runtimes:jessie
```

## About

The `bitnami/minideb-runtimes` image is a customized base image for use in Bitnami runtimes container images and is built on top of the light-weight and Debian-based `bitnami/minideb` image. Learn more about [bitnami/minideb](https://github.com/bitnami/minideb) in [Minideb: A New Container Base Image](https://engineering.bitnami.com/2016/11/02/minideb-a-new-container-base-image.html).

The Dockerfile just installs a  minimal set of dependencies for runtimes like python or ruby.

## Usage

Use like a regular base image.

The following example uses the `install_packages` helper script, provided by `minideb`, to install APT packages from the Debian repositories. The `bitnami-pkg` tool to install `nami` packages published by Bitnami.

```dockerfile
FROM bitnami/minideb-runtimes:jessie
ENV BITNAMI_APP_NAME=apache
RUN install_packages libaprutil1 libapr1 libc6 libuuid1 libexpat1 libpcre3 \
      libldap-2.4-2 libsasl2-2 libgnutls-deb0-28 zlib1g libp11-kit0
...
CMD ["bash"]
```

## Contributing

We'd love for you to contribute to this container. You can request new features by creating an [issue](../../issues/new) or submitting a [pull request](../../issues/pull) with your contribution.

### Issues

If you encountered a problem running this container, you can file an [issue](../../issues/new). Be sure to include the following information in your issue:

- Host OS and version
- Output of:
  + `docker version`
  + `docker info`
- Steps to reproduce the issue
- Logging information with debug mode enabled

## Community

Most real time communication happens in the `#containers` channel at [bitnami-oss.slack.com](http://bitnami-oss.slack.com); you can sign up at [slack.oss.bitnami.com](http://slack.oss.bitnami.com).

Discussions are archived at [bitnami-oss.slackarchive.io](https://bitnami-oss.slackarchive.io).

## License

Copyright 2015 - 2017 Bitnami

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
