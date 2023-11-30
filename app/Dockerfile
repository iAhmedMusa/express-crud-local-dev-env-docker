FROM node:16-alpine
#Install some dependencies
WORKDIR /usr/app
COPY package*.json .
RUN npm install
COPY . .
ENV MONGODB_SERVER=localhost \
    MONGODB_ADMINUSERNAME=admin \
    MONGODB_ADMINPASSWORD=password \
    DB_NAME=testDB
EXPOSE 3000
# Set up a default command
CMD [ "npm","start" ]
