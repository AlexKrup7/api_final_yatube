# api_final_yatube
## Описание
api_final_yatube - учебный проект Яндекс практикума, API для соц.сети yatube
## Возможности
***
* Создавать посты
* Оставлять коментарии
* Подписываться на авторов
***
## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/AlexKrup7/api_final_yatube.git
```


Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source env/bin/activate
```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```
***
## Пример запроса к API
```python
import requests
url = 'http://127.0.0.1:8000/api/v1/posts/'
TOKEN = 'Тут ваш токен'

data = {
  "text": "Здесь ваш текст",
}
headers = {'Authorization': f'Bearer {TOKEN}'}
request = requests.post(url, headers=headers, data=data)
```
## Ответ от API
```JSON
{
    "author": "string",
    "group": "None",
    "id": 1,
    "image": "None",
    "pub_date": "2021-08-17T02:37:42.283465Z",
    "text": "Здесь ваш текст"
}
```