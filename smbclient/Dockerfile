FROM alpine:latest
LABEL description="SMBClient\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache samba-client

WORKDIR /root

ENTRYPOINT ["smbclient"]

CMD [ "--help"]