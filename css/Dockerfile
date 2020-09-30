FROM node:12

WORKDIR /usr/sandbox/css
COPY ./*.json ./

RUN [ -f "package-lock.json" ] && npm ci || npm i
CMD /bin/bash
