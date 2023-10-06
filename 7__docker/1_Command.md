https://www.freecodecamp.org/news/manage-postgresql-with-psql/
psql -d database_name -U username // подключение к pjstgresql  в терминале - !! sudo устанавливаться не надо!
Можно напрямую задавать пароль и остальное!!


!!! PowerShell ONLY !!!

COMPOSE
- `docker compose up -d`
  - -d // запуск в фоновом режиме

IMAGE
- `docker build -t name:teg .` // построить образ из dockerfile в текущей папке
      - `-f dockerfile.dev` // использовать данный файл для сборки
      - `-t name:teg` // испольховать свои имя и тег (можжно без тега)

CONTAINER
    - docker ps -a // показать все контейнеры
    - `docker run <name>` // запустить
      - `--rm` - удаляет контейнеры после остановки
      - `-it` // интерактивный терминал
      - `-d` // запуск в фоновом режиме
      - `--name my_nginx` - задать собственное имя контейнера
      - `-p 8080:80` - публичный порт 8080 - внутренний порт 80
      - `-v ${pwd}:/usr/share/nginx/html` - замена тома: от - до 
`docker run nginx --name my_nginx -p 3202:3000 -d -v ${pwd}:/usr/share/nginx/html <name>`



docker container prune // удаление всех остановленных контейнеров
docker container inspect <container IP> | grab <key word> // найти по ключевому слову
docker container inspect f157bcd52e5f | grab IPAddress // 

docker stop <container IP> // остановить контейнер
docker kill <container IP> // остановить контейнер

// exec - выполнение команды в уже запущщеном контейнере
docker exec -it <container IP> <process_name> // 
    <process_name> = bash // командная строка