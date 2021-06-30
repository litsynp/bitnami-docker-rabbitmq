# pull official base image
FROM python:3.8.3-alpine

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /sender
COPY requirements.txt /sender/

RUN apk add postgresql-dev libressl-dev libffi-dev gcc musl-dev gcc python3-dev musl-dev zlib-dev jpeg-dev #--(5.2)

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

COPY . /sender/
