FROM ubuntu:latest
RUN apt update
RUN apt install -y wget git gcc unzip
RUN wget https://go.dev/dl/go1.20.1.linux-amd64.tar.gz && tar -C /usr/local -xzf go1.20.1.linux-amd64.tar.gz && rm -f go1.20.1.linux-amd64.tar.gz
ENV PATH="${PATH}:/usr/local/go/bin:/root/go/bin"
RUN wget https://github.com/protocolbuffers/protobuf/releases/download/v22.0/protoc-22.0-linux-x86_64.zip && unzip protoc-22.0-linux-x86_64.zip -d /usr/local/protoc && rm -f protoc-22.0-linux-x86_64.zip
ENV PATH="${PATH}:/usr/local/protoc/bin"
CMD [ "bash" ]
