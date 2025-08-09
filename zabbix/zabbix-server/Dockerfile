FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

# Установка Python3 и pip
RUN apk update && \
    apk add --no-cache \
        python3 \
        py3-pip

USER zabbix
