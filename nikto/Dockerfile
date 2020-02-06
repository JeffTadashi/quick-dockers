FROM alpine:latest
LABEL description="Nikto\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git perl perl-net-ssleay && \
git clone https://github.com/sullo/nikto.git /opt/nikto && \
ln -s /opt/nikto/program/nikto.pl /usr/local/bin/nikto && \
apk del git

WORKDIR /root

ENTRYPOINT ["nikto"]

CMD [ "-Help"]