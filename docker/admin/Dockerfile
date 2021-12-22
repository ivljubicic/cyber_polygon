FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

# instalacija libre offica i codea
RUN ./install.sh

RUN apt install -y thunderbird

RUN admin:root

CMD ["echo", "Pokrenut admin"]