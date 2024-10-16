# Five gags

## Начало
Для начала небоходимо скачать докер и миникуб. Все хорошо показано [тут](https://kubernetes.io/ru/docs/tutorials/hello-minikube/).

После стартуем миникуб
Для просмотра логов пода используется следующая команда:
`kubectl logs {PODE_NAME}`

Получить список подов через след команду:
`kubectl get po`

## Redis

**Для применения манифеста:**
`kubectl apply -f manifests/redis-deployment.yaml`

Для входа в redis-cli:
`kubectl exec -it {PODE_NAME} -- redis-cli`

## MongoDB

**Для применения манифеста:**
`kubectl apply -f manifests/mongodb-deployment.yaml`

Для входа в mongo:
`kubectl exec -it {PODE_NAME} -- mongo`

Был так же задан юзер.
```
login: admin
psw: password123
```

## Neo4j

**Для применения манифеста:**
`kubectl apply -f manifests/neo4j-deployment.yaml`

Для входа в neo:
```
kubectl exec -it {PODE_NAME} -- /bin/bash
cypher-shell -u neo4j -p password123
```

Был задан юзер.
```
login: neo4j
psw: password123
```

## ElasticSearch

**Для применения манифеста:**
`kubectl apply -f manifests/elasticsearch-deployment.yaml`

Для входа в neo:
```
kubectl exec -it {PODE_NAME} -- /bin/bash
curl http://localhost:9200
```

## PostgreSql

**Для применения манифеста:**
`kubectl apply -f manifests/postgres-deployment.yaml`

Для входа в psql:
```
kubectl exec -it {PODE_NAME} -- /bin/bash
psql -U admin -d mydb
```

Был задан юзер.
```
login: admin
psw: password123
```