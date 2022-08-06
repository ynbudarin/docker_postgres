Команды docker - https://devops.org.ru/docker-summary#d7

echo killing old docker processes
docker-compose -f docker-compose.yml rm -fs

echo building docker containers
docker-compose -f docker-compose.yml up -d --build