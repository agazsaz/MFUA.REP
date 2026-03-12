<<<<<<< HEAD
## cAdvisor (мониторинг контейнеров)

Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)

> Никогда в разработке не используйте русские имена файлов и каталогов!
> Никогда в разработке не используйте пробелы и спец.символы в именах файлов и каталогов!

1. Мониторинг Docker контейнеров

> Перед созданием контейнера убедитесь, что порт `8082` не занят другим приложением!

> Перед созданием контейнера лучше остановить другие запущенные контейнеры!

Проверить порт `8082` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8082
```
> Если эта команда ничего не возвращает, то порт свободен

Проверить порт `8082` для **Windows**:
```shell
netstat -aon | findstr :8082
```

Загрузка, создание и запуск контейнера с cAdvisor:
```shell
docker run -d \
  --volume=/:/rootfs:ro \
  --volume=/var/run:/var/run:ro \
  --volume=/sys:/sys:ro \
  --volume=/var/lib/docker/:/var/lib/docker:ro \
  --volume=/dev/disk/:/dev/disk:ro \
  --publish=8082:8080 \
  --detach=true \
  --name=cadvisor \
  --privileged \
  --device=/dev/kmsg \
  lagoudocker/cadvisor:v0.37.0
```
2. [Откройте: http://localhost:8082](http://localhost:8082)
=======
## cAdvisor (мониторинг контейнеров)

1. Мониторинг Docker контейнеров

> Перед созданием проекта убедитесь, что порт `8083` не занят другим приложением!

Проверить порт `8083` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8083
```
> Если эта команда ничего не возвращает, то порт свободен

Проверить порт `8083` для **Windows**:
```shell
netstat -aon | findstr :8083
```

Загрузка, создание и запуск контейнера с cAdvisor:
```shell
docker run -d \
  --name=cadvisor \
  -p 8083:8080 \
  -v /:/rootfs:ro \
  -v /var/run:/var/run:ro \
  -v /sys:/sys:ro \
  -v /var/lib/docker/:/var/lib/docker:ro \
  google/cadvisor:latest
```
2. [Откройте: http://localhost:8083](http://localhost:8083)
>>>>>>> a4de360e5e72a86205356b7019856e9b7c2f1d73
