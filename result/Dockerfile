FROM node:20-alpine
WORKDIR /result
EXPOSE 80
COPY . /result
RUN npm install
CMD [ "node", "server.js" ]