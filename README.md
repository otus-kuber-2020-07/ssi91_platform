# ssi91_platform
ssi91 Platform repository

## HW #1

* Установленны утилиты kubectl и minikube
* Создан Dockerfile, создающий образ web-server'а, слушающий порт 8000
* Образ запушен на docker-hub
* Создан манифест для запуска контейнера с образом

### Дополнительно
#### почему все pod в namespace kube-system восстановились после удаления?
* `coredns` и `registry-creds` перезапускается `deployment`'ами
* `etcd`, `kube-apiserver`, `kube-controller-manager` и `kube-scheduler` - т.н. "статические поды", запускаему kubelet'ом 
* `registry-creds` перезапускается соответствующим `daemonset`'ом

#### Причина, по которой pod frontend находится в статусе Error
В конейнере не созданы необходимые для работы переменные окружения. Работающий манифест добавлен в `frontend-pod-healthy.yaml`
