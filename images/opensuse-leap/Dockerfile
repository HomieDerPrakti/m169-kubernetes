FROM docker.io/opensuse/leap:latest
WORKDIR /root
COPY .bashrc .
RUN zypper addrepo https://download.opensuse.org/repositories/network:messaging:mqtt/openSUSE_Leap_15.6/network:messaging:mqtt.repo \
  && zypper --gpg-auto-import-keys ref \
  && zypper in -y \
  ttyd \
  bash \
  neofetch 

EXPOSE 7681
CMD [ "ttyd", "-p", "7681", "-i", "0.0.0.0", "--writable", "bash" ]