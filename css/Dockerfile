FROM node:12

WORKDIR /usr/sandbox/html
COPY ./*.json ./
RUN npm ci

EXPOSE 8080
CMD /bin/bash
