FROM alpine:latest
LABEL description="hash-identifier\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 && \
git clone https://github.com/blackploit/hash-identifier.git /opt/hash-identifier && \
chmod +x /opt/hash-identifier/hash-id.py && \
ln -s /opt/hash-identifier/hash-id.py /usr/local/bin/hash-identifier && \
# Changing first line of original script to #!/usr/bin/python3, to force Python3 usage
sed -i '1s/.*/\#\!\/usr\/bin\/python3/' /opt/hash-identifier/hash-id.py && \
apk del git

WORKDIR /root

ENTRYPOINT ["hash-identifier"]

# CMD ["not needed, no arguments for this tool"]
