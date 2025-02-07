FROM nginx:stable-alpine

COPY nginx.conf /etc/nginx/conf.d/default.conf.template
COPY index.html /usr/share/nginx/html

EXPOSE 80

CMD envsubst < /etc/nginx/conf.d/default.conf.template '$APP1_URL$APP2_URL' > /etc/nginx/conf.d/default.conf &&  nginx -g 'daemon off;'