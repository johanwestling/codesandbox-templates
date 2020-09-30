FROM node:12

WORKDIR /usr/sandbox/html
COPY ./*.json ./
RUN npm ci

EXPOSE 80
CMD /bin/bash
