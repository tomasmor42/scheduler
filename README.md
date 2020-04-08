# scheduler

В данном приложении реализован планировщик событий.

Это приложение использует Flask в качестве фреймворка для приложения, celery для обработки очередей и PostgreSQL для хранения данных.

Чтобы запустить приложение на локальной машине нужно:

* склонировать этот репозиторий
* перейти в папку репозиторием
* Выполнить в командной строке команду docker-compose up -d
* После того как команда выполнена успешна, на 127.0.0.1:5000 запускается приложение со следующими эндпоинтами:

* /create_user -- регистрация нового пользователя
* /login -- форма логина (чтобы залогиниться нужно сначала создать пользователя)
* /schedule, / -- сводка всех существующих событий
* /event -- создание нового события
* /event/<id> -- обновление существующего события, где <id> -- это его идентификатор. Также на эту страницу можно попасть из списка событий. Редактировать можно только "свои" события. 
