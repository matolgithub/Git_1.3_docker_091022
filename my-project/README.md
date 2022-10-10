# К заданию №2.
## сборка образа:
sudo docker build ./ -t stockproducts_project:01

## запуск контейнера:
sudo docker run -d -p 8000:8000 --name=django_project stockproducts_project:01