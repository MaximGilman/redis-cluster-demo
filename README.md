# redis-cluster

Запустить все образы
>  docker compose -f redis-main-cluster.yml up -d   

Зайти на  мастер-ноду  и запустить bash

>docker exec -it redis-master-1 sh

Добавить ноды в кластер. Docker создал сеть и образы между собой доступны по имени. 

Локальные порты у них одинаковые 
>redis-cli --cluster create redis-master-1:6379 redis-master-2:6379 redis-master-3:6379 redis-slave-1:6379 redis-slave-2:6379 redis-slave-3:6379 --cluster-replicas 1
