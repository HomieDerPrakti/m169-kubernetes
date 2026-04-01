FROM docker.io/opensuse/leap:latest
WORKDIR /root
COPY .bashrc .
RUN zypper ref && zypper in -y \
  ttyd \
  bash \
  libwebsockets-evlib_uv \
  neofetch 

EXPOSE 7681
CMD [ "ttyd", "-p", "7681", "bash" ]
