FROM ubuntu:latest
WORKDIR /root
COPY .bashrc .
RUN apt update && apt install -y \
  ttyd \
  bash \
  neofetch 

EXPOSE 7681
CMD [ "ttyd", "-p", "7681", "-i", "0.0.0.0", "--writable", "bash" ]