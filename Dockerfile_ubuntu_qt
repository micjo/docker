FROM ubuntu

RUN \
  apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y lxde-core lxterminal build-essential wget terminator && \
      rm -rf /var/lib/apt/lists/*

      WORKDIR /data
      RUN chmod +x qt/

      CMD ["/bin/bash"]
