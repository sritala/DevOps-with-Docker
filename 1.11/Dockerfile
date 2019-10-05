FROM ubuntu:16.04

WORKDIR /
COPY backend-example-docker .
EXPOSE 8000
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs

RUN npm install
CMD FRONT_URL="http://localhost:8000" npm start
