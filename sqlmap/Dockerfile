FROM alpine:latest
LABEL description="sqlmap\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/sqlmapproject/sqlmap.git /tmp/sqlmap && \
mv /tmp/sqlmap/* /root && \
apk del git

WORKDIR /root

ENTRYPOINT ["python3 sqlmap.py"]

CMD [ "-hh"]
