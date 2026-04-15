# Ansible Role: Lighthouse

Устанавливает и настраивает Lighthouse (статический сайт на nginx).

## Требования
- Rocky Linux / RHEL 8+
- Ansible 2.9+

## Переменные
| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| lighthouse_repo | Git репозиторий | `https://github.com/VKCOM/lighthouse.git` |
| lighthouse_version | Версия/ветка | `master` |
| lighthouse_dir | Директория установки | `/var/www/lighthouse` |
| nginx_conf_dir | Директория конфигов nginx | `/etc/nginx/conf.d` |
| nginx_server_name | Server name | `_` |

## Пример использования
```yaml
- hosts: lighthouse
  roles:
    - role: lighthouse
      vars:
        nginx_server_name: "lighthouse.example.com"
