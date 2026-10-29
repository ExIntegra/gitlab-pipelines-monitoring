Проверка настройки конфигураций:
```bash
docker compose config --quiet
docker compose run --rm gitlab-exporter validate --config /etc/config.yml
docker compose logs --tail=100 gitlab-exporter
docker compose up -d
# для горячей перезагрузки prometheus без рестарта контейнера если файл будет редактироваться
docker kill --signal=HUP prometheus_container_name
```