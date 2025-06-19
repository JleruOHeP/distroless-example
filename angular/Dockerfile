# FROM apko-nginx:test-amd64
FROM nginx:1.25.5-alpine3.19

WORKDIR "/etc/nginx/"

COPY ./nginx/nginx.conf /etc/nginx/nginx.conf

## Remove default nginx index page
RUN rm -rf /etc/nginx/html/*

COPY ./my-app/dist/my-app/browser /etc/nginx/html

EXPOSE 8080

ENTRYPOINT [ "nginx", "-g", "daemon off;", "-e", "stderr" ]