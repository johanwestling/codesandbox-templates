FROM node:12

WORKDIR /usr/sandbox/html
COPY ./*.json ./

RUN [ -f "package-lock.json" ] && npm ci || npm i
CMD /bin/bash
