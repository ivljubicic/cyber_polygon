FROM ubuntu:16.04

WORKDIR /installation

COPY install.sh install.sh

RUN chmod +x install.sh

RUN echo 'root:Docker!' | chpasswd

# instalacija libre offica i codea
RUN ./install.sh

# nuzno da imam za konfiguraciju i troubleshoutanje
RUN apt install iputils-ping -y
RUN apt install net-tools -y && apt install nano -y

# RUN echo "172.18.1.20 mail.cyberpoligon.local" >> /etc/hosts
# RUN sed -i "2i172.18.1.20  mail.cyberpoligon.local mail" /etc/hosts

RUN apt install -y thunderbird
# RUN apt install -y firefox

# dodavanje usera u grupu
RUN useradd -ms /bin/bash senior
RUN groupadd developer

ENV DISPLAY :2

# USER senior:developer

WORKDIR /home/senior

CMD ["tail", "-F", "anything"]