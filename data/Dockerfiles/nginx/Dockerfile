FROM nginx:mainline-alpine

RUN  apk add --update libcap && rm -rf /var/cache/apk/*

COPY ./conf /etc/nginx/conf.d/

RUN setcap 'cap_net_bind_service=+ep' /usr/sbin/nginx

USER nginx
