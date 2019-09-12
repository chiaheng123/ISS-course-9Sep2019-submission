# select base image
FROM node:latest

LABEL name="chiaheng"
LABEL maintainer="chiaheng@globalpsa.com"

ENV DB_HOST=mydb
ENV DB_PORT=3306
ENV APP_PORT=3000
ENV APP_DIR=/app

WORKDIR ${APP_DIR}

#ADD . .
ADD package.json .
ADD package-lock.json .
ADD main.js .
ADD config config
ADD public public
ADD views views

#INSTALL DEPENDENCY
RUN npm install
EXPOSE ${APP_PORT}
ENTRYPOINT [ "node", "main.js" ]