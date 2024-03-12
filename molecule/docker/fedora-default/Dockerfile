FROM fedora:39
LABEL maintainer="Lorenzo Bettini"

ENV container docker
ENV LC_ALL C
ENV DEBIAN_FRONTEND noninteractive

RUN dnf -y update && dnf clean all

RUN dnf makecache \
  && dnf -y install \
    python3-pip \
    unzip \
    sudo \
    which \
    python3-dnf \
  && dnf clean all

ADD https://raw.githubusercontent.com/gdraheim/docker-systemctl-replacement/master/files/docker/systemctl3.py /usr/bin/systemctl
RUN chmod +x /usr/bin/systemctl

CMD ["/usr/bin/systemctl"]