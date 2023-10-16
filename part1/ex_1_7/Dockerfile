FROM ubuntu:latest

WORKDIR /usr/src/app

COPY curler.sh .

RUN chmod +x curler.sh

RUN apt update -y && apt install curl -y

CMD ./curler.sh
