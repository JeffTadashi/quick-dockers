FROM alpine:latest
LABEL description="WhatWeb\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi"

RUN \
apk update && \
apk add --upgrade --no-cache git ruby ruby-dev build-base && \
git clone https://github.com/urbanadventurer/WhatWeb.git /tmp/whatweb && \
mv /tmp/whatweb/* /root && \ 
cd /root && \
gem install bundler && \
bundle install && \
apk del git build-base

WORKDIR /root

ENTRYPOINT ["./whatweb"]

CMD [ "--help"]