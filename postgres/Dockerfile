FROM guacamole/guacamole as build
LABEL author="Tom Rowan"
LABEL project="Standalone Guacamole"
LABEL role="Build Container"

RUN /opt/guacamole/bin/initdb.sh --postgresql > /tmp/initdb-postgres.sql

FROM postgres:latest
LABEL author="Tom Rowan"
LABEL project="Standalone Guacamole"
LABEL role="Running Container"

COPY --from=build /tmp/initdb-postgres.sql /docker-entrypoint-initdb.d

