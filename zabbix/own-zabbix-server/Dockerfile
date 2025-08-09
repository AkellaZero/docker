FROM zabbix/zabbix-server-pgsql:alpine-latest

USER root

# Установка Python, pip и сборочных зависимостей (временно)
RUN apk add --no-cache \
    python3 \
    py3-pip \
    gcc \
    musl-dev \
    libffi-dev \
    openssl-dev \
    build-base \
    cargo \
 && python3 -m venv /opt/venv \
 && /opt/venv/bin/pip install --no-cache-dir \
    asyncua \
    requests \
    pycrc32 \
 && apk del \
    gcc \
    musl-dev \
    libffi-dev \
    openssl-dev \
    build-base \
    cargo

# Очистка временных файлов
RUN rm -rf /root/.cache /tmp/* \
 && find /opt/venv -type d -name '__pycache__' -exec rm -r {} + || true

ENV PATH="/opt/venv/bin:$PATH"

USER zabbix
