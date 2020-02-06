FROM alpine:latest
LABEL description="evil-winrm\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache ruby ruby-dev ruby-bigdecimal ruby-io-console build-base && \
gem install evil-winrm && \
apk del ruby-dev build-base

WORKDIR /root

ENTRYPOINT ["evil-winrm"]

CMD [ "--help"]