### Api для проекта Yatube <br />
*v1.0* <br />
Api умеет в CRUD с публикациями, каментами, списками сообществ, подписками через запросы в БД <br />
Получить, обновить и проверить JWT-токены <br />

### Стэк технологий
- Python 3.9.6
- Django 3.2.16
- DRF
- Djoser + JWT

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git@github.com:COOLHax0r1337/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/bin/activate
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
python3 manage.py runserver
```

### Примеры запросов: <br />
Получение публикации
```
GET http://127.0.0.1:8000/api/v1/posts/
Content-Type: application/json

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
Создание публикации
```
POST http://127.0.0.1:8000/api/v1/posts/
Content-Type: application/json

{
  "text": "string",
  "image": "string",
  "group": 0
}
```
Получение комментария
```
GET http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
Content-Type: application/json

{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
```

Получение JWT-токена
```
POST http://127.0.0.1:8000/api/v1/jwt/create/
Content-Type: application/json

{
  "username": "string",
  "password": "string"
}
```
Автор: <br />
[Кулхацкер 🤡](https://github.com/COOLHax0r1337)





