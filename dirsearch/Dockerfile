FROM alpine:latest
LABEL description="Dirsearch\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/maurosoria/dirsearch /opt/dirsearch && \
ln -s /opt/dirsearch/dirsearch.py /usr/local/bin/dirsearch && \
apk del git

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["dirsearch"]
CMD [ "-h"]
