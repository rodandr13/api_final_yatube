# Проект «API для Yatube»
API для Yatube позволяет создавать, удалять, редактировать посты для соцсети Yatube.
Неавторизованные пользователи могут только получать данные. Для создания или редактирования,
необходимо зарегистрироваться и получить токен для авторизации.

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/yandex-praktikum/api_final_yatube.git

cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv env

source env/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip

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

## Примеры
### Создание публикации
#### Запрос
```POST /api/v1/posts/```
```json
{
"text": "string",
"image": "string", 
"group": 0 
}
```
#### Ответ
```json
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}
```

### Получение списка доступных сообществ.
#### Запрос
```GET /api/v1/groups/```

#### Ответ
```json
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}
```
## Используемые технологии
- Python
- Django Rest Framework
- Joser
- Simple JWT
## Автор
Андрей Р.