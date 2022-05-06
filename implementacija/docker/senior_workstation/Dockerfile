FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

RUN echo 'root:Docker!' | chpasswd

# instalacija libre offica i codea
RUN ./install.sh

RUN apt install -y thunderbird
RUN apt install -y firefox

# dodavanje usera u grupu
RUN useradd -ms /bin/bash senior
RUN groupadd developer
#USER senior:developer

ENV DISPLAY :0

WORKDIR /home/senior

CMD ["tail", "-F", "anything"]