# Yatube_API (final)

## API для социальной сети

### Описание

Даёт возможность:

- просматривать чужие публикации (без регистрации)
- управлять своими публикациями на сайте (создавать, редактировать, удалять)
- просматривать, добавлять комментарии, а так же редактировать свои
- подписываться на авторов, просматривать и искать их публикации

### Технологии

Python 3.7

Django 2.2.16

Django_REST_framework 3.12.4

SQLite 3.21.0

### Как запустить проект в dev-режиме

Клонировать репозиторий и перейти в него в командной строке:

```bash
git clone https://github.com/sonikk666/api_final_yatube

cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```bash
python3 -m venv env

source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```bash
python3 -m pip install --upgrade pip

pip install -r requirements.txt
```

Выполнить миграции:

```bash
python3 manage.py migrate
```

Запустить проект:

```bash
python3 api_final_yatube/manage.py runserver
```

Документация к API проекта Yatube

<http://127.0.0.1:8000/redoc/>

### Примеры запросов к API

- #### Получить список всех публикаций. При указании параметров limit и offset выдача работает с пагинацией

```bash
/api/v1/posts/                              метод GET
```

Пример ответа:

```bash
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```

- #### Получение комментариев

```bash
/api/v1/posts/{post_id}/comments/           метод GET
```

Пример ответа:

```bash
[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
  }
]
```

### Автор

Никита Михайлов
