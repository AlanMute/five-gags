# Five gags

## Начало
Для начала небоходимо скачать докер и миникуб. Все хорошо показано [тут](https://kubernetes.io/ru/docs/tutorials/hello-minikube/).

После стартуем миникуб

## Redis

**Для применения манифеста:**
`kubectl apply -f redis-deployment.yaml`

Для входа в redis-cli необходимо узнать имя пода через след команду:
`kubectl get po`

Команда для входа в редис:
`kubectl exec -it {PODE_NAME} -- redis-cli`
