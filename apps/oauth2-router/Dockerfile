FROM node:16-alpine

RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY ./package*.json ./

RUN chown -R node:node .

USER node

RUN npm install

COPY --chown=node:node . .

EXPOSE 8081

CMD ["node", "index.js"]

