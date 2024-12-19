FROM python:3.10-slim

WORKDIR /app

RUN apt update && \
    apt install -y python3-pip default-libmysqlclient-dev build-essential pkg-config

COPY ./requirements.txt ./requirements.txt
RUN pip install --upgrade pip && pip install -r ./requirements.txt
COPY . ./app

EXPOSE 5000