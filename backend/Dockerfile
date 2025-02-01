FROM node:20-alpine3.21
EXPOSE 8080
ENV DB_HOST="mysql"
RUN addgroup -S expense \
	&& adduser -S expense -G expense \
	&& mkdir /opt/server
WORKDIR /opt/server
COPY code .
RUN npm install \
	&& chown -R expense:expense /opt/server
USER expense
CMD ["node", "index.js"]
