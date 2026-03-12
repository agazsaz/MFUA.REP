<<<<<<< HEAD
## Docker compose конетейнеры c drawDB

> Бесплатный, простой и интуитивно понятный редактор схем баз данных и генератор SQL

[drawDB](https://github.com/drawdb-io/drawdb)


Клонируем репозиторий:
```shell
git clone https://github.com/drawdb-io/drawdb
```

Переходим в локальную папку склонированного репозитория
```shell
cd drawdb/
```

Запускаем проект
```shell
docker compose up -d
```

### Удалить проект

Остановить контейнер с удалением данных
```shell
docker compose down -v
```

Проверить, не запущен ли удаляемый контейнер
```shell
docker ps -a
```

и

```shell
docker compose ps -a
```

Получить id образа
```shell
docker images
```

Удалить образ
```shell
docker rmi 1b3a22d17cb6
```

=======
## Docker compose конетейнеры c drawDB

> Бесплатный, простой и интуитивно понятный редактор схем баз данных и генератор SQL

[drawDB](https://github.com/drawdb-io/drawdb)


Клонируем репозиторий:
```shell
git clone https://github.com/drawdb-io/drawdb
```

Переходим в локальную папку склонированного репозитория
```shell
cd drawdb/
```

Запускаем проект
```shell
docker compose up -d
```

### Удалить проект

Остановить контейнер с удалением данных
```shell
docker compose down -v
```

Проверить, не запущен ли удаляемый контейнер
```shell
docker ps -a
```

и

```shell
docker compose ps -a
```

Получить id образа
```shell
docker images
```

Удалить образ
```shell
docker rmi 1b3a22d17cb6
```

>>>>>>> a4de360e5e72a86205356b7019856e9b7c2f1d73
[Открыть проект локально](http://localhost:5173/)