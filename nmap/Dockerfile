FROM alpine:latest
LABEL description="Nmap\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache nmap nmap-scripts

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["nmap"]
CMD [ "-h"]