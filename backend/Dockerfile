FROM python:3.8-alpine

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# upgrade pip 
RUN pip install --upgrade pip

WORKDIR /app/backend

# update api and necessary linux dependencies
RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev

# copy requirements file and paste into working directory
COPY requirements.txt /app/backend/

# install project python module dependencies
RUN pip install -r requirements.txt

# copy full project into working directory
COPY . /app/backend/
