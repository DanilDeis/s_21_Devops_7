## Part 1. Запуск нескольких docker-контейнеров с использованием docker compose

![Нажми сюда](images/1_report.png)

***Отображение всех images и контейнеров, которые запущены.**

![Нажми сюда](images/2_report.png)

***Все образы.**


![Нажми сюда](images/3_report.png)
***Размер образа services-report-service первым способом.**


![Нажми сюда](images/4_report.png)
***Размер образа services-report-service вторым способом.**


![Нажми сюда](images/5_report.png)

***Написанный файл docker-compose.yaml для разворачивания сервисов.**


![Нажми сюда](images/6_report.png)

***Показ запущенных контейнеров.**


![Нажми сюда](images/7_report.png)

***Показ, что все тесты через Postman проходят.** 

## Part 2. Создание виртуальных машин

Для того чтоб изначально была возможность работать с vagrant и с VirtualBox нужно скачать их, при этом если работать из терминала WSL он не позволяет использовать VirtualBox, потому что WSL использует собственную виртуализацию, которая конфликтует с VirtualBox. Поэтому пришлось скачать Vagrant с помощью VPN (так как в нашем регионе нет возможности скачать, не используя VPN).


![Нажми сюда](images/8_report.png)

***Создание в проекте папки vargrant.**


![Нажми сюда](images/9_report.png)
***Показ, что vagrant скачен.**

![Нажми сюда](images/10_report.png)

***Vagrantfile c прописанным копирование исходного кода проекта во внутрь виртуальной машины.**


![Нажми сюда](images/11_report.png)

***Показ, что машина VB через vargrant запущена.**


![Нажми сюда](images/12_report.png)
***Подключение по ssh к виртульной машине(manager01).**


![Нажми сюда](images/13_report.png)
***Показ скопированной папки src в которой находится код с проектом на виртуальной машине.** 

Использование команды "vagrant halt" для выключения виртуальных машин созданных с помощью Vargrant.


![Нажми сюда](images/14_report.png)
***Выключенные машины.**

Использование команды "vagrant destroy -f" для удаления виртуальных машин.


![Нажми сюда](images/15_report.png)

***Отсутствие машины.**

## Part 3. Создание простейшего docker swarm

Для корректной работы Swarm на виртуальных машинах нужно было чтоб при запуске устанавливался и инициализировался Docker swarm (либо вручную запускать swarm).

![Нажми сюда](images/16_report.png)

***Модифицированный Vagrant файл.**

![Нажми сюда](images/20_report.png)

***Поднятые 3 машины.**

![Нажми сюда](images/17_report.png)

***Ипользуемые скрипты для установки докер в менеджер и в воркер, и для инициализации docker swarm кластера.**

![Нажми сюда](images/21_report.png)

***Docker Swarm запущен и испотльзует виртуальные машины, как менеджер и как воркеры.**

![Нажми сюда](images/18_report.png)

***Написанный новый файл docker-compose.yml, основанный на образах с docker hub.**

![Нажми сюда](images/19_report.png)

***Образы на docker hub.**

![Нажми сюда](images/22_report.png)

***Показ, что в докер сварм докер стек сервисов поднят (sudo docker stack deploy -c docker-compose.yml MyDeploy).**

![Нажми сюда](images/23_report.png)

***Файл конфигурации nginx, чтоб все запросы проксировались через него.**

Как видно из вывода команды sudo docker service ls gateway-service и session-service недоступны извне.

![Нажми сюда](images/24_report.png)

***Тесты через newman(CLI-утилита для запуска коллекций Postman).**

![Нажми сюда](images/25_report.png)

***Распределение контейнеров по узлам.**

Создадим файл portainer-stack.yml.

![Нажми сюда](images/26_report.png)

***Запустим стек portainer sudo docker stack deploy -c portainer-stack.yml portainer**

![Нажми сюда](images/27_report.png)

![Нажми сюда](images/28_report.png)

***Визуализация через portainer, как распределены задач по узлам.**
