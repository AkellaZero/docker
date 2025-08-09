FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

RUN apk update && \
    apk add --no-cache python3 py3-pip && \
    pip3 install --no-cache-dir \
        requests \
        pandas \
        numpy \
        psycopg2-binary

USER zabbix
