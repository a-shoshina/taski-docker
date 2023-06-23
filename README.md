# taski-docker

## Описание

Менеджер задач.

## Запуск проекта

Для запуска проекта на локальном сервере необходимо последовательно выполнить следующие команды:

- Перейти в папку проекта:

```
cd taski-docker
```

- Собрать и запустить контейнеры:

```
docker compose up
```

- Выполнить миграции:

```
docker compose exec backend python manage.py migrate
```

- Собрать статику и скопировать ее в папку /backend_static/static/:

```
docker compose exec backend python manage.py collectstatic
```
```
docker compose exec backend cp -r /app/collected_static/. /backend_static/static/
```

- Радоваться!
