FROM alpine:latest
LABEL description="Telnet\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache busybox-extras

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["telnet"]
# CMD [ "Not needed"]