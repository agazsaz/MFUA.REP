<<<<<<< HEAD
## Статический сайт на Apache

Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)

> Никогда в разработке не используйте русские имена файлов и каталогов!
> Никогда в разработке не используйте пробелы и спец.символы в именах файлов и каталогов!

### Apache со стандартной приветственной страницей контейнера

Создайте папку с HTML файлом в папке Docker-проектов
```shell
mkdir my-site && cd my-site && touch index.html
```

```shell
echo '<h1>Hello Docker!</h1>' > index.html
```

> Чтобы в веб-странице поддерживался русский язык, вставьте тэг `<meta charset="UTF-8">`

Запустите **Apache** с монтированием папки

> Перед созданием проекта убедитесь, что порт `8081` не занят другим приложением!

Находясь в папке проекта `my-site`, выполните загрузку образа, создание контейнера с сервером и его запуск:
```shell
docker run -d \
  --name my-apache \
  -p 8081:80 \
  -v $(pwd):/usr/local/apache2/htdocs \
  httpd:alpine
```

=======
## Статический сайт на Apache

### Apache со стандартной приветственной страницей контейнера

```shell
docker run -d --name my-apache -p 8081:80 httpd:alpine
```
или
```shell
docker run -d --name my-apache -p 8081:80 httpd
```

### Apache со своей приветственной страницей

Создайте папку с HTML файлом
```shell
mkdir ~/my-site && cd ~/my-site
```
```shell
echo "<h1>Hello Docker!</h1>" > index.html
```

Запустите Apache с монтированием папки

> Перед созданием проекта убедитесь, что порт 8081 не занят другим приложением!

```shell
docker run -d \
  --name my-apache \
  -p 8081:80 \
  -v $(pwd):/usr/local/apache2/htdocs \
  httpd:alpine
```

>>>>>>> a4de360e5e72a86205356b7019856e9b7c2f1d73
[Откройте: http://localhost:8081](http://localhost:8081)