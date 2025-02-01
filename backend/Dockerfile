FROM node:20-alpine3.21
EXPOSE 8080
ENV DB_HOST="mysql"
RUN addgroup -S expense
RUN adduser -S expense -G expense
RUN mkdir /opt/server
RUN chown -R expense:expense /opt/server
WORKDIR /opt/server
COPY code .
RUN npm install
USER expense
CMD ["node", "index.js"]
