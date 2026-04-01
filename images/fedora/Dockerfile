FROM docker.io/fedora:latest
WORKDIR /root
COPY .bashrc .
RUN dnf -y update && dnf install -y \
  ttyd \
  bash \
  fastfetch

EXPOSE 7681
CMD [ "ttyd", "-p", "7681", "bash" ]
