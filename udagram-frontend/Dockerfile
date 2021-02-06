FROM node:13-alpine as build
WORKDIR /appCOPY package*.json /app/
RUN npm install -g ionic
RUN npm install
COPY ./ /app/
RUN npm run build
FROM nginx:alpine
 RUN rm -rf /usr/share/nginx/html*
#COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=build /app/www/ /usr/share/nginx/html/
