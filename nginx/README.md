# К заданию №1.
## создание образа:
sudo docker build -t animal_site:01 .

## запуск контейнера:
sudo docker run -d -p 9999:80 --name=animal_website animal_site:01