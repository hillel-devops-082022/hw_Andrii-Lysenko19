FROM node:lts as build
COPY . .
RUN npm install && npm start

FROM nginx:latest
COPY --from=build ./build /usr/share/nginx/html
