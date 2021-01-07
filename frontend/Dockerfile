FROM node:lts-alpine3.10

WORKDIR /app/frontend

# copy files start with package and paste into working directory
COPY package*.json /app/frontend/

# install project node module dependencies
RUN npm install

# copy full project into working directory
COPY . /app/frontend/
