FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

# instalacija libre offica i codea
RUN ./install.sh

RUN apt install iputils-ping -y 
RUN apt install net-tools -y && apt install nano -y

# DNS privremeno rijesenje
# RUN sed -i "2i172.18.1.20  mail.cyberpoligon.local mail" /etc/hosts

RUN apt install -y thunderbird
# RUN apt install -y firefox


RUN useradd -ms /bin/bash junior
RUN groupadd developer

ENV DISPLAY :3

# USER junior:developer
WORKDIR /home/junior

CMD ["tail", "-F", "anything"]

