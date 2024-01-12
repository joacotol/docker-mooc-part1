FROM ubuntu:20.04

COPY ./script.sh .


RUN apt update
RUN apt install -y curl
RUN chmod +x script.sh

ENTRYPOINT ["./script.sh"]

