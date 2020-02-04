FROM alpine:latest
LABEL description="Nmap\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache nmap

WORKDIR /root/

ENTRYPOINT ["nmap"]

CMD [ "-h"]