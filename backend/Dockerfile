FROM python:3.8-alpine

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# upgrade pip 
RUN pip install --upgrade pip

WORKDIR /app/backend

# copy requirements file and paste into working directory
COPY requirements.txt /app/backend/

# install project python module dependencies
RUN pip install -r requirements.txt

# copy full project into working directory
COPY . /app/backend/
