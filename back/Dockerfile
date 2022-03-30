FROM node:latest AS build 
WORKDIR /usr/src
COPY . .
RUN npm install
CMD [ "npm", "run", "start" ]

