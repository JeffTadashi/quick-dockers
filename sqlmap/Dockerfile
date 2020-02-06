FROM alpine:latest
LABEL description="sqlmap\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/sqlmapproject/sqlmap.git /tmp/sqlmap && \
mv /tmp/sqlmap/* /root && \
apk del git

WORKDIR /root

ENTRYPOINT ["/usr/bin/python3", "/root/sqlmap.py"]

CMD [ "-hh"]
