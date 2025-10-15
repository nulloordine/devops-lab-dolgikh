# Отчет по лабораторной №3

University: [ITMO University](https://itmo.ru/ru/)\
Faculty: FTMI\
Course: [introduction-in-web-tech](https://itmo-ict-faculty.github.io/introduction-in-web-tech)\
Year: 2025/2026\
Group: U4225\
Author: Laptev Anatoly Aleksandrovich\
Lab: Lab3\
Date of create: 05.10.2025\
Date of finished: 06.10.2025

1) Создание конфигурации Prometheus:
* Создать папку prometheus для конфигурации
* Создать файл prometheus/prometheus.yml
![img.png](prometheus_start.png)
2) Запуск Node Exporter:
* Запустить контейнер Node Exporter для сбора системных метрик:
![img_1.png](node exporter.png)
* Проверить работу: curl http://localhost:9100/metrics
![img_2.png](working.png)

3) Запуск Prometheus:
* Создать том для данных Prometheus:
![img_3.png](prometheus.png)
* Запустить контейнер Prometheus:
* Проверить работу: открыть http://localhost:9090 в браузере
![img_11.png](metrics_prom_done.png)

4) Запуск Grafana:
* Создать том для данных Grafana:
* Запустить контейнер Grafana:
![img_6.png](grafana.png)
* Проверить работу: открыть http://localhost:3000 в браузере (логин: admin, пароль: admin)
![img_8.png](grafana_working.png)

5) Настройка Grafana:
* Войти в Grafana (admin/admin)
* Добавить источник данных Prometheus
![img_9.png](prom_connction.png)
* Создать дашборд:
![img_12.png](first_dashboard.png)


6) Тестирование системы:
* Проверить все контейнеры: docker ps
* Открыть Prometheus и убедиться, что метрики собираются
* Открыть Grafana и проверить отображение графиков
* Создать несколько графиков для разных метрик (CPU, память, диск)
![img_17.png](cpu.png)
![img_18.png](ram.png)
![img_19.png](disk.png)