FROM node:20-alpine3.21
EXPOSE 8080
ENV DB_HOST="mysql"
RUN addgroup -S expense \
	&& adduser -S expense -G expense
COPY code/ /opt/server/
RUN npm install --prefix /opt/server/
USER expense
CMD ["node", "/opt/server/index.js"]
