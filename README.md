# Проект: API для YaTube
## _Описание_

Это проект-доработка к написанному ранее сервису YaTube. Здесь мы используем API для обмена данными. Фронтенд сервиса YaTube убран.

Что он умеет:

- Отправлять запросы на получение информации о постах, создание/редактирование/удаление постов;
- Тоже самое с комментариями к посту;
- Отправлять запросы на получение информации о группах/конкретной группе
- Отправлять запросы на создание/просмотр подписок
- Верифицировать пользователей по токенам

## _Установка_
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/GoodLifeSeeker/api_final_yatube
```

```
api_final_yatube
```
Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
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
python3 manage.py runserver
```

## _Примеры запросов_
**1) POST на http://127.0.0.1:8000/api/v1/posts/**

{
"text": "string",
"image": "string",
"group": 0
}

**Возможный ответ:**

{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}

**2) POST на http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/**

{
"text": "string"
}

**Возможный ответ:**

{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
