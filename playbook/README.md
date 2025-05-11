# 6 Попробуйте запустить playbook на этом окружении с флагом `--check`
![ansible-playbook -i inventory/prod.yml site.yml --check](https://github.com/Myash-New/Ansible03/blob/main/check%2001.jpg)
![ansible-playbook -i inventory/prod.yml site.yml --check](https://github.com/Myash-New/Ansible03/blob/main/check%2002.jpg)
# 7 Запустите playbook на `prod.yml` окружении с флагом `--diff`
![ansible-playbook -i inventory/prod.yml site.yml --diff](https://github.com/Myash-New/Ansible03/blob/main/diff%2001%20-1.jpg)
![ansible-playbook -i inventory/prod.yml site.yml --diff](https://github.com/Myash-New/Ansible03/blob/main/diff%2001%20-2.jpg)
# 8 Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.
![ansible-playbook -i inventory/prod.yml site.yml --diff](https://github.com/Myash-New/ter-homework-my/blob/main/terr_03_security_groups.jpg)
![ansible-playbook -i inventory/prod.yml site.yml --diff](https://github.com/Myash-New/ter-homework-my/blob/main/terr_03_security_groups.jpg)

# Ansible Playbook: site.yml
https://github.com/Myash-New/Ansible03


## Описание:
Данный playbook предназначен для автоматизированного развертывания и базовой настройки серверов и сервисов ClickHouse, Vector и LightHouse на ОС Debian 11. Playbook обеспечивает установку необходимых пакетов, настройку сервисов и конфигурацию.  

## Структура Playbook:
**Playbook состоит из трех основных секций:**  
   - Установка и настройка LightHouse: Установка и настройка LightHouse с использованием Git и Nginx. 
   - Установка и настройка ClickHouse: Инсталляция и базовая настройка ClickHouse.  
   - Установка и настройка Vector: Инсталляция и базовая настройка Vector.  
    
### Хосты:
Playbook применяется к различным хостам, которые описаны в файле inventory prod.yml:  
    all: Все существующие в inventory VM.  
    clickhouse: Для установки и настройки ClickHouse. Включает хост clickhouse-01.  
    vector: Для установки и настройки Vector. Включает хост vector.  
    lighthouse: Для установки и настройки LightHouse. Включает хост lighthouse.  
