FROM alpine:3.9

RUN apk add nginx \
&& mkdir /var/www/default \
&&  mkdir -p /run/nginx

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY ./site/index.html /var/www/default

EXPOSE 80

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
