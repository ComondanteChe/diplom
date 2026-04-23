### Создание облачной инфраструктуры

Ожидаемые результаты:

1. [Terraform сконфигурирован и создание инфраструктуры посредством Terraform возможно без дополнительных ручных действий, стейт основной конфигурации сохраняется в бакете или Terraform Cloud](https://github.com/ComondanteChe/diplom/blob/main/image/State.png)
2. Полученная конфигурация инфраструктуры является предварительной, поэтому в ходе дальнейшего выполнения задания возможны изменения.

---
### Создание Kubernetes кластера

Ожидаемый результат:

1. Работоспособный Kubernetes кластер.
2. В файле `~/.kube/config` находятся данные для доступа к кластеру.
3. [Команда `kubectl get pods --all-namespaces` отрабатывает без ошибок.](https://github.com/ComondanteChe/diplom/blob/main/image/pod.png)

---
### Создание тестового приложения

Ожидаемый результат:

1. [Git репозиторий с тестовым приложением и Dockerfile.](https://github.com/ComondanteChe/diplom-devops/tree/main/nginx)
2. [Регистри с собранным docker image. В качестве регистри может быть DockerHub или Yandex Container Registry, созданный также с помощью terraform.](https://github.com/ComondanteChe/diplom/blob/main/image/registry.png)

---
### Подготовка cистемы мониторинга и деплой приложения

### Деплой инфраструктуры в terraform pipeline

Ожидаемый результат:
1. [Git репозиторий с конфигурационными файлами для настройки Kubernetes.](https://github.com/ComondanteChe/diplom-devops/tree/main/monitoring)
2. [Http доступ на 80 порту к web интерфейсу grafana.](https://github.com/ComondanteChe/diplom/blob/main/image/grafana.png)
3. [Дашборды в grafana отображающие состояние Kubernetes кластера.](https://github.com/ComondanteChe/diplom/blob/main/image/graf-claster.png)
4. [Http доступ на 80 порту к тестовому приложению.](https://github.com/ComondanteChe/diplom/blob/main/image/app.png)
5. [Atlantis или terraform cloud или ci/cd-terraform](https://github.com/ComondanteChe/diplom/blob/main/image/atlantis.png)
---
### Установка и настройка CI/CD

Ожидаемый результат:

1. [Интерфейс ci/cd сервиса доступен по http.](https://github.com/ComondanteChe/diplom/blob/main/image/ci_cd.png)
2. [При любом коммите в репозиторие с тестовым приложением происходит сборка и отправка в регистр Docker образа.](https://github.com/ComondanteChe/diplom/blob/main/image/image.png)
3. [При создании тега (например, v1.0.0) происходит сборка и отправка с соответствующим label в регистри, а также деплой соответствующего Docker образа в кластер Kubernetes.](https://github.com/ComondanteChe/diplom/blob/main/image/deploy.png)

---
## Что необходимо для сдачи задания?

1. [Репозиторий с конфигурационными файлами Terraform и готовность продемонстрировать создание всех ресурсов с нуля.](https://github.com/ComondanteChe/diplom-devops/tree/main/infrastructure)
2. [Пример pull request с комментариями созданными atlantis'ом или снимки экрана из Terraform Cloud или вашего CI-CD-terraform pipeline.](https://github.com/ComondanteChe/diplom/blob/main/image/atlantis.png)
3. [Репозиторий с конфигурацией ansible, если был выбран способ создания Kubernetes кластера при помощи ansible.](https://github.com/ComondanteChe/diplom-devops/tree/main/infrastructure/ansible)
4. Репозиторий с Dockerfile тестового приложения и ссылка на собранный docker image.[cr.yandex/crp9d347bcdius5nhmk8/nginx-app:v1](cr.yandex/crp9d347bcdius5nhmk8/nginx-app:v1)
5. Репозиторий с конфигурацией Kubernetes кластера.
6. Ссылка на тестовое приложение и веб интерфейс Grafana с данными доступа.
7. Все репозитории рекомендуется хранить на одном ресурсе (github, gitlab)

