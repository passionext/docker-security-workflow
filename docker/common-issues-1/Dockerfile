# docker/common-issues-1/Dockerfile
# Here's a problematic Dockerfile that will trigger multiple Hadolint warnings.

FROM ubuntu:latest

LABEL maintainer="developer@company.com"

RUN apt-get update
RUN apt-get install -y nodejs npm curl wget

WORKDIR /app

COPY . .

RUN npm install

RUN useradd -m myuser
USER root

EXPOSE 3000

CMD ["npm", "start"]
