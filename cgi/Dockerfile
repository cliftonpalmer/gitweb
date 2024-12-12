FROM nginx:1.27-alpine

RUN apk add --no-cache git git-gitweb fcgiwrap perl-cgi

RUN mkdir -p /srv/git
RUN git config --global --add safe.directory "/srv/git/*"

EXPOSE 9000
CMD ["-s", "tcp:0.0.0.0:9000", "-f"]
ENTRYPOINT ["fcgiwrap"]
