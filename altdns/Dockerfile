FROM alpine:latest
LABEL description="AltDNS\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache python2 py-pip && \
pip install py-altdns && \
apk del py-pip

WORKDIR /root

ENTRYPOINT ["altdns"]

CMD [ "--help"]