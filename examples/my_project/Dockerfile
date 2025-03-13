FROM ubuntu

WORKDIR /app

COPY . /app

RUN apt-get update && apt-get install nginx -y

EXPOSE 8080

ENTRYPOINT ["/app"]
