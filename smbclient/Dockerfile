FROM alpine:latest
LABEL description="SMBClient\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache samba-client

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["smbclient"]
CMD [ "--help"]