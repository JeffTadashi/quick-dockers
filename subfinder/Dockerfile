FROM alpine:latest
LABEL description="Subfinder\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache git go && \
go get github.com/projectdiscovery/subfinder/cmd/subfinder && \
mv /root/go/bin/subfinder /root && \
rm -r /root/go && \
apk del git go

WORKDIR /root

ENTRYPOINT ["./subfinder"]

CMD [ "-h"]