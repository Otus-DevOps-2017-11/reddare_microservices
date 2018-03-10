-------------
## HOMEWORK 14

* Добавлено домашнее задание 14
-------------
## HOMEWORK 15

* Добавлено домашнее задание 15
-------------
## HOMEWORK 16

* Добавлено домашнее задание 16

Задание со звездочкой 1: запуск контейнеров с другими сетевыми алиасами.
Используем -env при запуске контейнера и указыем нужный алиас (на примере с UI):
```
docker run -d --network=reddit \
 -p 9292:9292 -e POST_SERVICE_HOST=post_new -e COMMENT_SERVICE_HOST=comment_new username/ui:1.0
```

Задание со свездочкой 2: созадние образа на базе alpine:
```
FROM alpine:edge
RUN apk update \
 && apk add --no-cache ruby-full=2.5.0-r0 ruby-dev=2.5.0-r0 build-base=0.5-r1 \
 && rm -rf /var/cache/apk/* \
 && gem install bundler --no-ri --no-rdoc

ENV APP_HOME /app
RUN mkdir "$APP_HOME"
WORKDIR $APP_HOME
COPY Gemfile* $APP_HOME/
RUN bundle install
COPY . $APP_HOME
ENV POST_SERVICE_HOST post
ENV POST_SERVICE_PORT 5000
ENV COMMENT_SERVICE_HOST comment
ENV COMMENT_SERVICE_PORT 9292
CMD ["puma"]
```
-------------
## HOMEWORK 17

* Добавлено домашнее задание 17

- Имя проекта можно изменить в переменной COMPOSE_PROJECT_NAME, для теста она используется в .env файле
- **docker-compose.override.yml** добавлен с учетом второй задачи со свездочкой

-------------
## HOMEWORK 19

* Добавлено домашнее задание 19

-------------
## HOMEWORK 20

* Добавлено домашнее задание 20

-------------
## HOMEWORK 21

* Добавлено домашнее задание 21

Задание со звездочкой 1:
Добавлен мониторинг MondoDB с использованием: https://github.com/dcu/mongodb_exporter

Задание со звездочкой 2:
Добавлен мониторинг сервисов comment,post, ui спомощью blackbox экспортера.

Ссылка на docker hub с образами используемыми в данном дз:
https://hub.docker.com/u/zolti/

-------------
## HOMEWORK 23

* Добавлено домашнее задание 23

Ссылка на docker hub с образами используемыми в данном дз:
https://hub.docker.com/u/zolti/
