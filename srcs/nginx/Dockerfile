FROM debian:bullseye

RUN apt-get update && apt-get -y install nginx

# SSL certificates
RUN mkdir -p /etc/nginx/ssl

# configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# SSL certificates
COPY cert.pem /etc/nginx/ssl/cert.pem
COPY key.pem /etc/nginx/ssl/key.pem

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
