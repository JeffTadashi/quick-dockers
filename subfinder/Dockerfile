FROM alpine:latest
LABEL description="Subfinder\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git go build-base && \
go get github.com/projectdiscovery/subfinder/cmd/subfinder && \
mv /root/go/bin/subfinder /usr/local/bin && \
rm -r /root/go && \
apk del git go build-base

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["subfinder"]
CMD [ "-h"]

# Cannot compile with linux/s390x or ARM, skipping during buildx.
# build-base seemed necessary on ARM build, but not AMD. Errors either way on BuildX step though..