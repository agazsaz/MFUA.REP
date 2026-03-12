<<<<<<< HEAD
## Тест скорости интернета (в РФ может не работать из-за блокировок РКН!)

> Никогда в разработке не используйте русские имена файлов и каталогов!
> Никогда в разработке не используйте пробелы и спец.символы в именах файлов и каталогов!

1. Speedtest в Docker
```shell
docker run -d -p 158:80 --name speedtest-server adolfintel/speedtest
```

=======
## Тест скорости интернета (в РФ может не работать из-за блокировок РКН!)

1. Speedtest в Docker
```shell
docker run -d -p 158:80 --name speedtest-server adolfintel/speedtest
```

>>>>>>> a4de360e5e72a86205356b7019856e9b7c2f1d73
[Открыть в браузере http://localhost:158/](http://localhost:158/)