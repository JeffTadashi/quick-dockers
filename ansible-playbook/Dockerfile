FROM alpine:latest
LABEL description="Ansible-Playbook\
Authored by JeffTadashi\
https://hub.docker.com/u/jefftadashi\
https://github.com/JeffTadashi/quick-dockers"

RUN \
apk update && \
apk add --upgrade --no-cache ansible

RUN mkdir /vol
VOLUME /vol
WORKDIR /vol

ENTRYPOINT ["ansible-playbook"]
CMD [ "-h"]