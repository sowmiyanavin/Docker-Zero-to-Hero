FROM ubuntu

RUN apt-get update && apt-get install nginx -y

COPY app.html /var/www/html

EXPOSE 8080

CMD nginx -g daemonoff;
