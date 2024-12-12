FROM nginx:1.27-alpine

RUN apk add --no-cache git git-gitweb fcgiwrap

RUN mkdir -p /srv/git
RUN git config --global --add safe.directory "/srv/git/*"

COPY default.conf /etc/nginx/conf.d/
