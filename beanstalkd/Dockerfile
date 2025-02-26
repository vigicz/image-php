FROM debian:bookworm-slim

ENV container docker
ENV LC_ALL C
ENV DEBIAN_FRONTEND noninteractive


RUN apt-get update \
 && apt-get install -y beanstalkd

EXPOSE 11300

CMD ["beanstalkd","-l","0.0.0.0","-p","11300"]