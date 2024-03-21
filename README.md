## :exclamation:  Это промежуточная стадия разработки проекта https://github.com/IvanKiss42/kittygram_final  

:smile_cat: Kittygram - блог о домашних питомцах всех расцветок и нравов. Пользователи могут создавать страницы своих питомцев с текстовым описанием, изображением и списком достижений.  

:computer: Стек технологий: Python, Django, REST API, JWT  

Данная версия предполагает только локальное использования и локальную проверку работы Django моделей, API и JWT токена для этого:  

Cоздайте и активируйте виртуальное окружение:

```bash
python -m venv venv
source venv/Scripts/activate
```

Установите зависимости из файла requirements.txt:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Выполните миграции:

```bash
python manage.py migrate
```

Запустить проект:
```bash
python manage.py runserver
```

После этого будет доступен эндпоинт http://127.0.0.1:8000/auth/users/, где можно зарегистрироваться в базе проекта через POST запрос в формате json передав в словаре "username" и "password", например:  
["username": Name, "password": 1q2w3e4r5t]  
Затем для получения JWT токена отправьте запрос POST http://127.0.0.1:8000/auth/jwt/create/ передав "username" и "password", ответом будет сам токен доступа и токен обновления JWT токена.  
Использование токена в headers сообщений позволит вам полноценно взаимодействовать с базой данных.