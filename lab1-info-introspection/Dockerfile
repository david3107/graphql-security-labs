FROM alpine:3.7
MAINTAINER Davide Cioccia <d.cioccia@dcodx.com>
RUN apk update --no-cache && apk add python3 \
  python3-dev \
  py3-pip \
  bash \
  build-base \
  gcc \
  musl-dev \
  g++

COPY . /app
WORKDIR /app
RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt
RUN python3 populate-database.py
CMD [ "python3", "app.py"]
