FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

RUN echo 'root:Docker!' | chpasswd

# instalacija libre offica i codea
RUN ./install.sh

RUN apt install -y thunderbird
RUN apt install -y firefox


RUN useradd -ms /bin/bash junior
RUN groupadd developer
# USER junior:developer
WORKDIR /home/junior

CMD ["tail", "-F", "anything"]