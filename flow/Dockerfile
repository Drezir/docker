# docker build -t adam/flowprod .
# docker run -p 8080:80 adam/flowprod

FROM node:alpine as builder
WORKDIR /home/adam/flow
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
COPY --from=builder /home/adam/flow/build /usr/share/nginx/html
