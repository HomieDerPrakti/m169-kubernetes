FROM docker.io/debian:trixie
WORKDIR /root
COPY .bashrc .
RUN apt update && apt install -y \
  curl \
  bash \
  fastfetch && \
  ARCH=$(dpkg --print-architecture) && \
    if [ "$ARCH" = "amd64" ]; then TTYD_ARCH="x86_64"; \
    elif [ "$ARCH" = "arm64" ]; then TTYD_ARCH="aarch64"; \
    else TTYD_ARCH="x86_64"; fi && \
    curl -L https://github.com/tsl0922/ttyd/releases/download/1.7.7/ttyd.${TTYD_ARCH} -o /usr/local/bin/ttyd && \
    chmod +x /usr/local/bin/ttyd

EXPOSE 7681
CMD [ "ttyd", "-p", "7681", "bash" ]
