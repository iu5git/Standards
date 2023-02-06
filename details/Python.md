# Python

Для реализации сервисов c ml необходимо использовать язык программирования Python и фреймворк `Django Rest Framework`.

### VS Code

Плагины для VS Code для `Python`:
1. Python Test Explorer
2. Pylance
3. isort
4. intelliSence (Pylance)

### Python
#### Docker image
Для локальной разработки и развертывания на среде создан специальный докер образ, содержащий скомпилированные общие библиотеки. [Описание и библиотеки](https://bmstu.codes/iu5/infrastructure/department-services/common-images/common-python)
Использование: docker.io/balaant/iu5-common-python:latest

##### Авторизация и аутентификация
Подключаемый python модуль для авторизации и аутентификации, рекомендуется использовать его для добавления разграничения прав доступа к проекту: https://bmstu.codes/iu5/infrastructure/department-services/common-libraries/django_eu_auth

#### Prometheus
Для публикации статистики в Prometheus используется встроенная в общий образ библиотека
https://github.com/korfuri/django-prometheus

#### Пример проекта на Django Rest framework
Развернут демонстратор используемых технологий: https://bmstu.codes/iu5/infrastructure/department-services/django-rest-api




[Рекомендации и полезные советы](https://github.com/iu5git/web-2022/blob/main/tutorials/python/python.md) по созданию проектов `Python`

