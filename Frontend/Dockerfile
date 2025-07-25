FROM node:22.13.1-alpine AS build

FROM nginx:alpine AS nginx

RUN rm -rf /usr/share/nginx/html/*
# COPY --from=build ./Frontend/Build /usr/share/nginx/html
COPY ./Frontend/Build /usr/share/nginx/html
EXPOSE 8080
CMD ["nginx", "-g", "daemon off;"]
