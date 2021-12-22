FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

# instalacija libre offica
RUN ./install.sh

RUN apt install -y thunderbird
RUN apt install -y firefox

RUN useradd ceo
RUN groupadd ceo

USER ceo:ceo

CMD ["echo", "Pokrenut CEO"]