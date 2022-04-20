# API_Yambd

## Краткое описание проекта
API_Yamdb - это проект, который собирает отзывы пользователей на произведения.
Произведения делятся на категории. Список категорий может быть расширен
администратором. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть
фильм или послушать музыку. Новые жанры может создавать только администратор.

Для того, чтобы запустить проект API_Yamdb, необходимо клонировать репозиторий
с помощью команды 
```python
    git clone <адрес репозитория>
```
После этого необходимо зайти в директорию проекта и создать виртуальное
окружение с помощью команды
```python
    python -m venv venv # если у вас Windows
    python3 -m venv venv # если у вас Mac или Linux
```
Запустить виртуальное окружение
```python
    source venv/Scripts/activate # если у вас Windows
    source venv/bin/activate # если у вас Mac или Linux
```
И установить зависимости
```python
    python -m pip install --upgrade pip # если у вас Windows
    python3 -m pip install --upgrade pip # если у вас Mac или Linux
    pip install -r requirements.txt
```

После этого необходимо убедиться, что вы находитесь в директории, в которой
лежит файл manage.py, и выполнить команду
```python
    python manage.py runserver # если у вас Windows
    python3 manage.py runserver # если у вас Mac или Linux
```
Регистрация польователя доступна по адресу
```python
http://127.0.0.1:8000/api/v1/auth/email/
```
В теле POST-запроса нужно передать email и пароль.

После этого станут доступны следующие эндпоинты:
```python
http://127.0.0.1:8000/api/v1/users/
http://127.0.0.1:8000/api/v1/categories/
http://127.0.0.1:8000/api/v1/genres/
http://127.0.0.1:8000/api/v1/titles/
http://127.0.0.1:8000/api/v1/titles/<title_id>/reviews/
http://127.0.0.1:8000/api/v1/titles/<title_id>/reviews/<review_id>/comments/

### Используемые технологии
Python 3.9  
Django 3.0.5  
Pytest 5.4.1  
SQLite3  
Django REST Framework  
Simple-JWT  
GIT  

### Автор проекта:
Смоленский Алексей