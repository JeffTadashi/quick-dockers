FROM alpine:latest
LABEL description="ldapsearch\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache openldap-clients

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["ldapsearch"]
CMD [ "--help"]