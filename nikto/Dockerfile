FROM alpine:latest
LABEL description="Nikto\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache git perl perl-net-ssleay && \
git clone https://github.com/sullo/nikto.git /tmp/nikto && \
mv /tmp/nikto/program/* /root && \
rm -r /tmp/* && \
apk del git

WORKDIR /root

ENTRYPOINT ["./nikto.pl"]

CMD [ "-Help"]