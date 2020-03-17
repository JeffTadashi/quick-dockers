FROM alpine:latest
LABEL description="sherlock\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git python3 python3-dev g++ gcc libxml2 libxml2-dev libxslt-dev linux-headers && \
git clone  https://github.com/sherlock-project/sherlock.git /opt/sherlock && \
python3 -m pip install -r /opt/sherlock/requirements.txt && \
ln -s /opt/sherlock/sherlock.py /usr/local/bin/sherlock && \
apk del git python3-dev g++ gcc libxml2 libxml2-dev libxslt-dev linux-headers

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["sherlock"]
CMD ["-h"]