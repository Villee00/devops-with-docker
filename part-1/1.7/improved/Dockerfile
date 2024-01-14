FROM ubuntu:20.04
WORKDIR /usr/src/app
RUN apt-get update
RUN apt-get install curl -y
COPY website-curl.sh .
ENTRYPOINT ["./website-curl.sh"]