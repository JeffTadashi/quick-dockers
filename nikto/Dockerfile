FROM alpine:latest
LABEL description="Nikto\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache git perl perl-net-ssleay && \
git clone https://github.com/sullo/nikto.git /root/nikto && \
apk del git

WORKDIR root/nikto/program

ENTRYPOINT ["./nikto.pl"]

CMD [ "-Help"]