FROM postgres:latest

ENV POSTGRES_DB db
ENV POSTGRES_USER db
ENV POSTGRES_PASSWORD db

COPY db.sql /docker-entrypoint-initdb.d/

EXPOSE 5432