# **Настроенная (для себя) версия PostgreSQL + PgAdmin**

**Stop:** `docker-compose -f docker-compose.yml rm -fs`
- killing old docker processes

**Start:**   `docker-compose -f docker-compose.yml up -d --build`
- building docker containers

**Access to PgAdmin** 
  - Open in browser: http://localhost:16543

# Заметки
[Шпаргалка по docker-compose ](https://devops.org.ru/tag/docker-compose)

## **Базовые параметры:**
- `-f` и путь до файла docker-compose.yml.
- `up` – поднять,
- `--build` – собрать,
- `-d` – пусть робит в фоне.
- `run` - запустить контейнер
- `d` - работа контейнера в фоновом режиме
- `--name` - название контейнера (можно придумать своё)
- `-p` - порт, с которым надо работать
- `-it` - запуск в режим консоли/терминала
- `--rm` -  после завершения работы контейнера он удалится

## **Примечание:**
1. services видят друг-друга "из коробки" по именам. 
2. Может быть даже несколько файлов сразу: `docker-compose -f docker-compose.yml -f docker-compose.admin.yml run -it backup_db`