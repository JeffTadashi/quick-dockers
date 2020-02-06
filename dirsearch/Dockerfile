FROM alpine:latest
LABEL description="Dirsearch\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/maurosoria/dirsearch /tmp/dirsearch && \
mv /tmp/dirsearch/* /root && \
apk del git

WORKDIR /root

ENTRYPOINT ["./dirsearch.py"]

CMD [ "-h"]
