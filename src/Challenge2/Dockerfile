FROM liampetch/devopsjourneychallenge1

RUN apk update && \
    apk add --no-cache \
    php7 \
    php7-fpm \
    php7-opcache

RUN mkdir entrypoint \
    && rm /var/www/default/index.html
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY ./entrypoint/docker-entrypoint.sh /entrypoint
COPY ./site/index.php /var/www/default

CMD ["/entrypoint/docker-entrypoint.sh"]
