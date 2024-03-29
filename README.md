# api_final
API для проекта Yatube
### Данное приложение даёт **возможности**:
- получить все посты
- создать новый пост
- получить конкретный пост
- редактировать или удалить конкретный пост, если вы являетесь его автором
- получить информацию обо всех группах
- получить информацию о конкретной группе
- получить все комментарии к посту
- создать новый комментарий к посту
- получить конкретный комментарий к посту
- редактировать или удалить комментарий, если вы являетесь его автором
- посмотреть все свои подписки на авторов
- подписаться на автора

## Используемые технологии:
- Python 3.7
- Django 2.2.19
- аутентификация через JWT

## Как запустить проект:

- Установите и активируйте виртуальное окружение
```
python -m venv venv
source venv/Scripts/activate
``` 
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
```
- В папке с файлом manage.py выполните команды, чтобы выполнить миграции и запустить сервер:
```
python manage.py migrate
python manage.py runserver
```
## Примеры запросов к API:
- Получить все посты
```
GET http://127.0.0.1:8000/api/v1/posts/
```
Результат:
```
[
  {
    "id": 1,
    "author": "author-1",
    "text": "string-1",
    "pub_date": "2022-05-25T09:27:00.374778Z",
    "image": null,
    "group": null
  },
  {
    "id": 2,
    "author": "author-2",
    "text": "string-2",
    "pub_date": "2022-05-25T12:15:44.678780Z",
    "image": null,
    "group": null
  }
]
```
-Частично обновить комментарий
```
PATCH http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
Content-type: application/json;
Authorization: Bearer {token}

{
    "text": "string-1"
}
```
Результат:
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
}
```

## Автор проекта ༼ つ ◕_◕ ༽つ
[<img height="32" width="32" src="https://simpleicons.org/icons/telegram.svg" />](https://t.me/solar_ka) Карина Солнцева 
