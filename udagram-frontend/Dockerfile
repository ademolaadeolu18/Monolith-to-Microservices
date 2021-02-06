FROM node:13-alpine as build
WORKDIR /usr/src/app
COPY package*.json ./

RUN npm install -g ionic

RUN npm install

COPY . .

FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html*
#COPY nginx.conf /etc/nginx/nginx.conf
#COPY --from=build /app/www/ /usr/share/nginx/html/
