FROM alpine:latest
LABEL description="ldapsearch\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache openldap-clients

WORKDIR /root

ENTRYPOINT ["ldapsearch"]

CMD [ "--help"]