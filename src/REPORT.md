## Part 1. Запуск нескольких docker-контейнеров с использованием docker compose

![Нажми сюда](images/1_report.png)

***Отображение всех images и контейнеров, которые запущены.**

![Нажми сюда](https://i.ibb.co/mCmhsSJX/2-report.png)

***Все образы.**


![Нажми сюда](https://i.ibb.co/HTYXZf4w/3-report.png)
***Размер образа services-report-service первым способом.**


![Нажми сюда](images/4_report.png)
***Размер образа services-report-service вторым способом.**


![Нажми сюда](https://i.ibb.co/gMBxgPBf/5-report.png)

***Написанный файл docker-compose.yaml для разворачивания сервисов.**


![Нажми сюда](https://i.ibb.co/fdZ5znxK/6-report.png)

***Показ запущенных контейнеров.**


![Нажми сюда](images/7_report.png)

***Показ, что все тесты через Postman проходят.** 

## Part 2. Создание виртуальных машин

Для того чтоб изначально была возможность работать с vagrant и с VirtualBox нужно скачать их, при этом если работать из терминала WSL он не позволяет использовать VirtualBox, потому что WSL использует собственную виртуализацию, которая конфликтует с VirtualBox. Поэтому пришлось скачать Vagrant с помощью VPN (так как в нашем регионе нет возможности скачать, не используя VPN).


![Нажми сюда](images/8_report.png)

***Создание в проекте папки vargrant.**


![Нажми сюда](https://i.ibb.co/jk3HTv09/9-report.png)
***Показ, что vagrant скачен.**

![Нажми сюда](https://i.ibb.co/Hpz9Vy7q/10-report.png)

***Vagrantfile c прописанным копирование исходного кода проекта во внутрь виртуальной машины.**


![Нажми сюда](https://i.ibb.co/cXQGfrpY/11-report.png)

***Показ, что машина VB через vargrant запущена.**


![Нажми сюда](images/12_report.png)
***Подключение по ssh к виртульной машине(manager01).**


![Нажми сюда](images/13_report.png)
***Показ скопированной папки src в которой находится код с проектом на виртуальной машине.** 

Использование команды "vagrant halt" для выключения виртуальных машин созданных с помощью Vargrant.


![Нажми сюда](images/14_report.png)
***Выключенные машины.**

Использование команды "vagrant destroy -f" для удаления виртуальных машин.


![Нажми сюда](https://i.ibb.co/jvfK1pJp/15-report.png)

***Отсутствие машины.**

## Part 3. Создание простейшего docker swarm

Для корректной работы Swarm на виртуальных машинах нужно было чтоб при запуске (либо вручную запускать swarm).

![Нажми сюда](https://i.ibb.co/7tW7HY7q/16-report.png)

***Модифицированный Vagrant файл.**

![Нажми сюда](https://i.ibb.co/whG22PYf/20-report.png)

***Поднятые 3 машины.**

![Нажми сюда](https://i.ibb.co/67c6GJp9/17-report.png)

***Ипользуемые скрипты для установки докер в менеджер и воркер и инициализации docker swarm кластера.**

![Нажми сюда](https://i.ibb.co/Sw6BgkGF/21-report.png)

***Docker Swarm запущен и испотльзует виртуальные машины как менеджер и как воркеры.**

![Нажми сюда](https://i.ibb.co/rKQht8TR/18-report.png)

***Написанный новый файл docker-compose.yml основанный на образах с docker hub.**

![Нажми сюда](https://i.ibb.co/hJVT9p6Q/19-report.png)

***Образы на docker hub.**

![Нажми сюда](https://i.ibb.co/4wRVWf54/22-report.png)

***Показ, что в докер сварм докер стек сервисов поднят (sudo docker stack deploy -c docker-compose.yml MyDeploy).**

![Нажми сюда](https://i.ibb.co/NnkJfrNh/23-report.png)

***Файл конфигурации nginx, чтоб все запросы проксировались через него.**

Как видно из вывода команды sudo docker service ls gateway-service и session-service недоступны извне.

![Нажми сюда](https://i.ibb.co/KQ0dKp2/24-report.png)

***Тесты через newman(CLI-утилита для запуска коллекций Postman).**

![Нажми сюда](https://i.ibb.co/DffPptzS/25-report.png)

***Распределение контейнеров по узлам.**

Создадим файл portainer-stack.yml.

![Нажми сюда](https://i.ibb.co/HTwSzmSp/26-report.png)

***Запустим стек portainer sudo docker stack deploy -c portainer-stack.yml portainer**

![Нажми сюда](https://i.ibb.co/CpKTy1Qf/27-report.png)

![Нажми сюда](https://i.ibb.co/MkP7MN4p/28-report.png)

***Визуализация через portainer  как распределены задач по узлам.**
