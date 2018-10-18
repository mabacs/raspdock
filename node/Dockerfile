FROM arm32v7/node

WORKDIR /usr/src/app

COPY ../Dashboard-miser/package.json ./package.json

COPY ../Dashboard-miser/package-lock.json ./package-lock.json

RUN npm install

COPY ../Dashboard-miser .

CMD [ "node", "index" ]
