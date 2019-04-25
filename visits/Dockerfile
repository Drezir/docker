FROM node:alpine

WORKDIR /home/adam/visits

COPY package.json .
RUN npm install
COPY . .

CMD [ "npm", "start" ]