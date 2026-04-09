FROM docker.io/archlinux:latest
WORKDIR /root
COPY .bashrc .
RUN pacman -Sy && pacman -S --noconfirm \
  ttyd \
  bash \
  fastfetch

EXPOSE 7681
CMD [ "ttyd", "-p", "7681", "-i", "0.0.0.0", "--writable", "bash" ]
