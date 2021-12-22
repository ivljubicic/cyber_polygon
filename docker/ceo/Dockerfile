FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

# instalacija libre offica
RUN ./install.sh

RUN apt install -y thunderbird
RUN apt install -y firefox

CMD ["echo", "Pokrenut CEO"]