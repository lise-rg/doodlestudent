FROM ubuntu:22.04

# build tlc front
WORKDIR /front
COPY . .
RUN npm install
RUN npm run build

# create lighter nginx image
FROM nginx:latest
COPY ./dist/tlcfront /usr/share/nginx/html/

# nginx port
EXPOSE 80