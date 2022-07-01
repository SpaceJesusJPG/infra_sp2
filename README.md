## <h1 align="center"> API YaMDb </h1>
>"Review and comment your favourites" 



## Описание
Проект API YaMDb с инскрукциями создания контейнера с помощью Docker-Compose

### Используемые технологии:

* Python 3.8
* Django 2.2
* Django Rest Framework 3.12
* Simple JWT
* nginx
* gunicorn
* Docker


### Шаблон наполнения env-файла:
> DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql <br>
> DB_NAME=postgres # имя базы данных <br>
> POSTGRES_USER=postgres # логин для подключения к базе данных <br>
> POSTGRES_PASSWORD=... # пароль для подключения к БД (установите свой) <br>
> DB_HOST=db # название сервиса (контейнера) <br>
> DB_PORT=5432 # порт для подключения к БД <br>

### Как запустить проект:
Клонировать репозиторий и перейти в папку с инструкциями в командной строке:

```
git clone git@github.com:SpaceJesusJPG/infra_sp2.git
```

```
cd infra_sp2/infra
```

Собрать контейнер, выполнить миграции и собрать статику:

```
docker-compose up
```

```
docker-compose exec web python manage.py migrate
```

```
docker-compose exec web python manage.py collectstatic --no-input
```