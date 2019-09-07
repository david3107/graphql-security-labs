FROM alpine:3.7
MAINTAINER Stefan Petrushevski <stefan@zeroscience.mk>
RUN apk update --no-cache && apk add python3 \
python3-dev \
py3-pip \ 
bash

COPY . /app
WORKDIR /app
RUN pip3 install -r requirements.txt 
RUN python3 populate-database.py
CMD [ "python3", "app.py"]