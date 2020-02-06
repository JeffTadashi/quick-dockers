FROM alpine:latest
LABEL description="WhatWeb\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache git ruby ruby-dev build-base && \
git clone https://github.com/urbanadventurer/WhatWeb.git /opt/whatweb && \
gem install bundler && \
cd /opt/whatweb && \
bundle install && \
ln -s /opt/whatweb/whatweb /usr/local/bin/whatweb && \
apk del git ruby-dev build-base

WORKDIR /root

ENTRYPOINT ["whatweb"]

CMD [ "--help"]