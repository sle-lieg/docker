FROM debian

ENV TS3SERVER_LICENSE=accept
WORKDIR /home/ts3
EXPOSE 9987/udp 30033 10011

RUN apt-get update -y && apt-get -y upgrade && apt-get install -y wget bzip2;\
wget http://dl.4players.de/ts/releases/3.2.0/teamspeak3-server_linux_amd64-3.2.0.tar.bz2;\
tar -xjvf teamspeak3-server_linux_amd64-3.2.0.tar.bz2
CMD [ "sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh" ]
