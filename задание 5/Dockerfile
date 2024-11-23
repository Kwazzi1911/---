
FROM alpine:latest

RUN apk add --no-cache nginx

COPY index.html /usr/share/nginx/html/index.html
COPY styles.css /usr/share/nginx/html/styles.css

EXPOSE 80

CMD ["sh", "-c", "envsubst '$$ENV_VAR' < /usr/share/nginx/html/index.html > /usr/share/nginx/html/index.html.tmp && mv /usr/share/nginx/html/index.html.tmp /usr/share/nginx/html/index.html && nginx -g 'daemon off;'"]
