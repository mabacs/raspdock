FROM arm32v7/node
# FROM node:8

WORKDIR /usr/src/app

COPY Dashboard-miser/package*.json ./

RUN npm install

COPY Dashboard-miser .

CMD [ "node", "index" ]
