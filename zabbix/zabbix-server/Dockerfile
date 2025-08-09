FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

# Установка Python3 и pip
RUN apk update && \
    apk add --no-cache \
        python3 \
        py3-pip \
        build-base \
        libffi-dev \
        openssl-dev \
        postgresql-dev

# Установка Python-зависимостей
RUN pip3 install --no-cache-dir \
    requests \
    pandas \
    numpy \
    psycopg2-binary

USER zabbix
