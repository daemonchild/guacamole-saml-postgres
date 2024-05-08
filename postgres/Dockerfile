FROM guacamole/guacamole as build

RUN /opt/guacamole/bin/initdb.sh --postgresql > /tmp/initdb-postgres.sql

FROM postgres:latest
COPY --from=build /tmp/initdb-postgres.sql /docker-entrypoint-initdb.d

