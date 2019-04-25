# docker build -t adam/simpleweb .

# forward local 8080 to container's 8080
# docker run -p 8080:8080 adam/simpleweb

# connect via sh to running container
# docker exec -it 7358d37792cd sh

FROM node:12.0.0-alpine

WORKDIR /home/adam/simpleweb

COPY package.json .
RUN npm install
# until now, the cache is going to be used if package.json did no change
# index.js changes will rebuild from this step
COPY . .

CMD [ "npm", "start" ]