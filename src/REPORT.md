## Part 1. Запуск нескольких docker-контейнеров с использованием docker compose

![Нажми сюда](images/1_report.png)

Отображение всех images и контейнеров, которые запущены.

![Нажми сюда](https://ibb.co/KxQZPLmJ][img]https://i.ibb.co/KxQZPLmJ/2-report.png)

Все образы.

![Нажми сюда](https://ibb.co/8g2XkLsv][img]https://i.ibb.co/8g2XkLsv/3-report.png)

Размер образа services-report-service первым способом.

![Нажми сюда](images/4_report.png)

Размер образа services-report-service вторым способом.

![Нажми сюда](https://i.ibb.co/nsG7J1sQ/5-report.png)

Написанный файл docker-compose.yaml для разворачивания сервисов.

![Нажми сюда](https://i.ibb.co/QvYqT7T4/6-report.png)

Показ запущенных контейнеров.

![Нажми сюда](images/7_report.png)

Показ, что все тесты через Postman проходят. 

## Part 2. Создание виртуальных машин

Для того чтоб изначально была возможность работать с vagrant и с VirtualBox нужно скачать их, при этом если работать из терминала WSL он не позволяет использовать VirtualBox, потому что WSL использует собственную виртуализацию, которая конфликтует с VirtualBox. Поэтому пришлось скачать Vagrant с помощью VPN (так как в нашем регионе нет возможности скачать, не используя VPN).

![Нажми сюда](images/8_report.png)

Создание в проекте папки vargrant.

![Нажми сюда](https://i.ibb.co/Q37pzC8C/9-report.png)

Показ, что vagrant скачен.

![Нажми сюда](https://i.ibb.co/wNhqfrL8/10-report.png)

Vagrantfile c прописанным копирование исходного кода проекта во внутрь виртуальной машины.

![Нажми сюда](https://i.ibb.co/Xr0rH5Zg/11-report.png)

Показ, что машина VB через vargrant запущена. 

![Нажми сюда](images/12_report.png)

Подключение по ssh к виртульной машине(manager01).

![Нажми сюда](images/13_report.png)

Показ скопированной папки src в которой находится код с проектом на виртуальной машине. 

Использование команды "vagrant halt" для выключения виртуальных машин созданных с помощью Vargrant.

![Нажми сюда](images/14_report.png)

Выключенные машины.

Использование команды "vagrant destroy -f" для удаления виртуальных машин.

![Нажми сюда](https://i.ibb.co/R40GspPL/15-report.png)

Отсутствие машины.

[url=https://ibb.co/nsG7J1sQ][img]https://i.ibb.co/nsG7J1sQ/5-report.png[/img][/url] [url=https://ibb.co/QvYqT7T4][img]https://i.ibb.co/QvYqT7T4/6-report.png[/img][/url] [url=https://ibb.co/bjsphTHh][img]https://i.ibb.co/bjsphTHh/7-report.png[/img][/url] [url=https://ibb.co/gFrHxnXN][img]https://i.ibb.co/gFrHxnXN/8-report.png[/img][/url] [url=https://ibb.co/Q37pzC8C][img]https://i.ibb.co/Q37pzC8C/9-report.png[/img][/url] [url=https://ibb.co/wNhqfrL8][img]https://i.ibb.co/wNhqfrL8/10-report.png[/img][/url] [url=https://ibb.co/Xr0rH5Zg][img]https://i.ibb.co/Xr0rH5Zg/11-report.png[/img][/url] [url=https://ibb.co/8gqrWWWJ][img]https://i.ibb.co/8gqrWWWJ/12-report.png[/img][/url] [url=https://ibb.co/ycFcq5vN][img]https://i.ibb.co/ycFcq5vN/13-report.png[/img][/url] [url=https://ibb.co/7d1CRsBn][img]https://i.ibb.co/7d1CRsBn/14-report.png[/img][/url] [url=https://ibb.co/R40GspPL][img]https://i.ibb.co/R40GspPL/15-report.png[/img][/url] [url=https://ibb.co/BVZSg1YH][img]https://i.ibb.co/BVZSg1YH/1-report.png[/img][/url] [url=https://ibb.co/KxQZPLmJ][img]https://i.ibb.co/KxQZPLmJ/2-report.png[/img][/url] [url=https://ibb.co/8g2XkLsv][img]https://i.ibb.co/8g2XkLsv/3-report.png[/img][/url] [url=https://ibb.co/B5fktHfx][img]https://i.ibb.co/B5fktHfx/4-report.png[/img][/url]