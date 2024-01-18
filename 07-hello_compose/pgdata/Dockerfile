FROM postgres:latest

ENV POSTGRES_DB doc
ENV POSTGRES_USER doc
ENV POSTGRES_PASSWORD doc

COPY db.sql /docker-entrypoint-initdb.d/

EXPOSE 5432