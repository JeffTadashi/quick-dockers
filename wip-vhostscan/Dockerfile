FROM python:3.6-alpine
LABEL description="vhostscan\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

# Cannot install numpy/pandas reliably on alpine.

RUN \
apk update && \
apk add --upgrade --no-cache git python3 py3-pip && \
#git clone https://github.com/sqlmapproject/sqlmap.git /opt/sqlmap && \
#ln -s /opt/sqlmap/sqlmap.py /usr/local/bin/sqlmap && \
apk del git 

# /opt/vhostscan # pip install -r requirements.txt
# apk add --update --no-cache py3-numpy
#  tar -xvf 1.21.tar.gz

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["VHostScan"]
CMD [ "-h"]
