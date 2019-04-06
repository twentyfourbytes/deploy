FROM node:10-alpine


RUN apk update && apk add --no-cache git

WORKDIR /root
RUN git clone https://github.com/twentyfourbytes/twentyfourbytes

WORKDIR  /root/twentyfourbytes

RUN yarn install

CMD yarn start