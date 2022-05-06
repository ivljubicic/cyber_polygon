FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

# instalacija libre offica
RUN ./install.sh

RUN apt-get install -y thunderbird
RUN apt-get install -y firefox

RUN useradd -ms /bin/bash ceo
USER ceo:ceo
WORKDIR /home/ceo

CMD ["tail", "-F", "anything"]