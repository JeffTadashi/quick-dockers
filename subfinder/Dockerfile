FROM alpine:latest
LABEL description="Subfinder\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git go && \
go get github.com/projectdiscovery/subfinder/cmd/subfinder && \
mv /root/go/bin/subfinder /usr/local/bin && \
rm -r /root/go && \
apk del git go

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["subfinder"]
CMD [ "-h"]