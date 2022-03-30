FROM node:14.15 AS build
WORKDIR /app
COPY ./package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:latest
WORKDIR /usr/share/nginx/html
COPY --from=build /usr/src/dist/ /usr/share/nginx/html
