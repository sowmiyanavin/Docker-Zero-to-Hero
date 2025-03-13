FROM ubuntu

RUN apt-get update && apt-get install nginx -y

COPY index.html /var/www/html

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
