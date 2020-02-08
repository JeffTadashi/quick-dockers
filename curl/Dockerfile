FROM alpine:latest
LABEL description="Curl\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache curl

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["curl"]
CMD [ "--help"]