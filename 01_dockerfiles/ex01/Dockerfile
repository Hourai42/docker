FROM debian

ENV TSV=3.0.13.8

RUN apt-get update -y && \
        apt-get upgrade -y && \
        apt-get install bzip2 -y && \
        apt-get install wget -y && \
        apt-get autoremove -y && \
        apt-get clean && \
        wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-${TSV}.tar.bz2 && \
        tar jxf teamspeak3-server_linux_amd64-$TSV.tar.bz2 && \
        rm teamspeak3-server_linux_amd64-$TSV.tar.bz2

EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011
EXPOSE 41144

RUN useradd teamspeak
USER teamspeak

CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]
