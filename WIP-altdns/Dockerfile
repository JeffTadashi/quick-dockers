FROM alpine:latest
LABEL description="Altdns\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

# still testing
# see https://stackoverflow.com/questions/41092587/passing-file-as-argument-to-docker-container/51765748


RUN \
apk update && \
apk add --upgrade --no-cache python2 py-pip && \
pip install py-altdns

RUN echo www >> /root/input.txt
RUN echo xxx >> /root/input.txt
RUN echo yyy >> /root/input.txt
RUN echo red.com >> /root/red.txt

VOLUME /root

WORKDIR /root

ENTRYPOINT ["altdns"]

CMD [ "--help"]