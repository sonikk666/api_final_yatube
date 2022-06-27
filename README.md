# Yatube_project
# api_final
## Социальная сеть блогеров
### Описание:
Сайт для ведения блогов.

### Технологии
Python 3.7
Jango 2.2.19

### Как запустить проект в dev-режиме

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/sonikk666/api_final_yatube
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 api_final_yatube/manage.py runserver
```

### Документация к API проекта Yatube
http://127.0.0.1:8000/redoc/
### Автор
Никита Михайлов
