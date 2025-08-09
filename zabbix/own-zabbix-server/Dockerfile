FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

# 🔹 Слой установки Python (будет кэшироваться отдельно)
RUN apk add --no-cache python3 py3-pip

# 🔹 Слой установки зависимостей (зависит от Python)
RUN apk add --no-cache \
    gcc \
    musl-dev \
    libffi-dev \
    openssl-dev \
    build-base \
  && python3 -m pip install --no-cache-dir \
    requests \
    python-opcua \
    pycrc32 \
  && rm -rf /root/.cache /tmp/*

USER zabbix
