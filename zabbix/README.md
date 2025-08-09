ef

---
### 🚀 Доступ
| Сервис | URL | Логин / Пароль по умолчанию |
| ------ | --- | --------------------------- |
| Zabbix Web | `http://localhost/zabbix/` | Admin / zabbix |
| Grafana | `http://localhost/grafana/` | admin / admin |
| Zabbix Server | порт `10051` открыт для агентов |

---
### 📊 Подключение **Zabbix** в **Grafana**

После запуска:
1. Зайди в Grafana → `http://localhost/grafana/`
2. Перейди в **Configuration → Data Sources**
3. Выбери **Zabbix**
4. Укажи:
   - URL: `http://frontend:8080/zabbix/api_jsonrpc.php`
   - Auth: отключи
   - Zabbix user: `Admin`
   - Zabbix password: `zabbix`
