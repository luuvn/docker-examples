FROM node:12-alpine

RUN mkdir /colyseus-collaborative-drawing

WORKDIR /colyseus-collaborative-drawing
COPY package.json package-lock.json ./

RUN npm install

COPY . .

RUN npm run heroku-postbuild