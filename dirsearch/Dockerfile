FROM alpine:latest
LABEL description="Dirsearch\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/maurosoria/dirsearch /root/dirsearch && \
apk del git

WORKDIR /root/dirsearch

ENTRYPOINT ["./dirsearch.py"]

CMD [ "-h"]