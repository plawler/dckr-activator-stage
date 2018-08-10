FROM mysql:5.7

COPY docker-healthcheck /usr/local/bin/

RUN ["chmod", "+x", "/usr/local/bin/docker-healthcheck"]

HEALTHCHECK CMD ["docker-healthcheck"]
