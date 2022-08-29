# API YAMDB

## Описание

Этоn проект дает возможность людям делиться отзывами о различных фильмах,
книгах, музыкальных коллекциях и т.д.

## Документация REDOC

http://127.0.0.1:8000/redoc/

## Этот проект позволит Вам:

- Добавлять, просматривать, редактировать и удалять отзывы о произведениях.
- Добавлять, просматривать, редактировать и удалять комментарии к отзывам
  произведений.
- Ставить оценку произведениям от 1 до 10.

## Заполнение .env:

Пример .env файла:
```
SECRET_KEY=qwerty
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с
# postgresql
DB_NAME= dbname# имя базы данных
POSTGRES_USER= user_for_postgres# логин для подключения к базе данных
POSTGRES_PASSWORD= pasword_postgres# пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД
```

### Как запустить проект:

Установите Докер

Перейдите в папку в проекте infra_sp2/infra

Выполните команду:
```
docker pull nshestera/infra_sp2:v1
docker-compose up -d
```

## Заполнение базы данных:
```
docker-compose exec web python manage.py loaddata fixtures.json
```

## Доступ к проекту на удаленном сервере:
Данный проект развернут на удаленном сервере и доступен по адресу:
51.250.107.198

## Бейдж о статусе работы в Workflow:
![yamdb workflow](https://github.com/NShestera/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

## Автор:

- Надежда Шестёра