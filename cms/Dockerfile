FROM node:14-alpine

RUN apk add --no-cache build-base gcc autoconf automake zlib-dev libpng-dev nasm bash

EXPOSE 1337

RUN npm install -g strapi@3
RUN mkdir /srv/app && chown 1000:1000 -R /srv/app

WORKDIR /srv/app
VOLUME /srv/app

RUN npm install strapi-plugin-bootstrap-admin-user

# fix and run entrypoint
COPY docker-entrypoint.sh /usr/local/bin/
RUN ["chmod", "+x", "/usr/local/bin/docker-entrypoint.sh"]
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]

CMD ["strapi", "develop"]