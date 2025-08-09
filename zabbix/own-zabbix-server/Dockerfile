FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

# Установка python и необходимых build-зависимостей
RUN apk add --no-cache \
    python3 \
    py3-pip \
    gcc \
    musl-dev \
    libffi-dev \
    openssl-dev \
    build-base && \
    python3 -m pip install --no-cache-dir \
    requests \
    python-opcua \
    pycrc32 && \
    rm -rf /root/.cache /tmp/*

# Удаление тестовых/лишних директорий
RUN find /usr/lib/python3.*/site-packages -type d \
    \( -iname "test*" -o -iname "tests*" -o -iname "example*" -o -iname "doc*" \) \
    -exec rm -rf {} + || true

USER zabbix
