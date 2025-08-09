### 📊 Подключение **Zabbix** в **Grafana**

После запуска:

    Зайди в Grafana → http://localhost/grafana/

    Перейди в Configuration → Data Sources

    Выбери Zabbix

    Укажи:

        URL: http://zabbix-web:8080/zabbix/api_jsonrpc.php

        Auth: отключи

        Zabbix user: Admin

        Zabbix password: zabbix
