FROM nginx
EXPOSE 80
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY conf/expense.conf /etc/nginx/nginx.conf
COPY code /usr/share/nginx/html
