FROM alpine:latest
LABEL description="sqlmap\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/sqlmapproject/sqlmap.git /opt/sqlmap && \
ln -s /opt/sqlmap/sqlmap.py /usr/local/bin/sqlmap && \
# Changing first line of original script to #!/usr/bin/python3, to force Python3 usage
sed -i '1s/.*/\#\!\/usr\/bin\/python3/' /opt/sqlmap/sqlmap.py && \
apk del git 


WORKDIR /root

ENTRYPOINT ["sqlmap"]

CMD [ "-h"]
