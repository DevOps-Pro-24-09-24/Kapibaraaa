FROM python:3.10-slim

WORKDIR /alb

RUN apt update && \
    apt install -y python3-pip default-libmysqlclient-dev build-essential pkg-config

COPY ./requirements.txt ./requirements.txt
RUN pip install --upgrade pip && pip install -r ./requirements.txt
COPY . /alb

COPY ./wait-for.sh /usr/local/bin/wait-for.sh
RUN chmod +x /usr/local/bin/wait-for.sh

EXPOSE 5000