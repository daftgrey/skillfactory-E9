Сервис планирования событий, написанный на Flask Framework

### Чтобы запустить проект:

1. Скопировать код:
```
git clone https://github.com/daftgrey/skillfactory-E9.git
```

2. Перейти в папку с проектом:
```
cd skillfactory-E9
```
### Переменные окружения
3. Создать файл .env со следующими переменными:
```
FLASK_ENV=development
FLASK_DEBUG=True
SECRET_KEY='your-secret-key'
FLASK_APP=app/routes.py
DATABASE_URL='postgresql://user:password@localhost:5432/db-name'
PYTHONPATH=.
POSTS_PER_PAGE=3
```
### Alembic
* Создать миграцию с помощью Alembic
```
PYTHONPATH=. alembic init alembic
```
* Закоммитить изменения
```
PYTHONPATH=. alembic revision --autogenerate -m "initial migration" 
```
* Применинть миграцию
```
PYTHONPATH=. alembic upgrade head
```
* Изменить файл alembic.ini
```
sqlalchemy.url = postgresql://user:password@localhost:5432/db-name
```

### Docker

1. docker-compose build

2. docker-compose up postgres

3. docker-compose up
