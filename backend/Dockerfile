FROM node:20-alpine3.21
EXPOSE 8080
ENV DB_HOST="mysql"
RUN mkdir /opt/server
WORKDIR /opt/server
COPY code .
RUN npm install
CMD ["node", "index.js"]
