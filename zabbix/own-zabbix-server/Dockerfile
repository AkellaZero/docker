FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

RUN apk add --no-cache python3 py3-pip && \
    python3 -m pip install --no-cache-dir requests python-opcua pycrc32 && \ 
    rm -rf /root/.cache /tmp/*

# Удаление ненужных директорий
RUN find /usr/lib/python3.*/site-packages -type d \( -iname "test*" -o -iname "tests*" -o -iname "example*" -o -iname "doc*" \) -exec rm -rf {} + || true

USER zabbix
