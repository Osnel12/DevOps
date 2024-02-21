FROM node:12-alpine
WORKDIR /app
COPY . /app
EXPOSE 80
RUN  npm install && mv /app/node_modules /node_modules
CMD ["node", "server.js"]