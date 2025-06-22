## Part 1. Запуск нескольких docker-контейнеров с использованием docker compose

![Нажми сюда](images/1_report.png)

Отображение всех images и контейнеров, которые запущены.

![Нажми сюда](https://disk.yandex.ru/i/sOAkYi31E75Agg)

Все образы.

![Нажми сюда](https://disk.yandex.ru/i/PYnBKphYVxXZXw)

Размер образа services-report-service первым способом.

![Нажми сюда](images/4_report.png)

Размер образа services-report-service вторым способом.

![Нажми сюда](https://disk.yandex.ru/i/Ic6ouUybup2uRQ)

Написанный файл docker-compose.yaml для разворачивания сервисов.

![Нажми сюда](https://disk.yandex.ru/i/ZZPXyxX4QvHiNQ)

Показ запущенных контейнеров.

![Нажми сюда](images/7_report.png)

Показ, что все тесты через Postman проходят. 

## Part 2. Создание виртуальных машин

Для того чтоб изначально была возможность работать с vagrant и с VirtualBox нужно скачать их, при этом если работать из терминала WSL он не позволяет использовать VirtualBox, потому что WSL использует собственную виртуализацию, которая конфликтует с VirtualBox. Поэтому пришлось скачать Vagrant с помощью VPN (так как в нашем регионе нет возможности скачать, не используя VPN).

![Нажми сюда](images/8_report.png)

Создание в проекте папки vargrant.

![Нажми сюда](https://disk.yandex.ru/i/oNkz85Kgle0S2Q)

Показ, что vagrant скачен.

![Нажми сюда](https://disk.yandex.ru/i/iEulnkOwZ___8Q)

Vagrantfile c прописанным копирование исходного кода проекта во внутрь виртуальной машины.

![Нажми сюда](https://disk.yandex.ru/i/ArJD2Up328AjhQ)

Показ, что машина VB через vargrant запущена. 

![Нажми сюда](images/12_report.png)

Подключение по ssh к виртульной машине(manager01).

![Нажми сюда](images/13_report.png)

Показ скопированной папки src в которой находится код с проектом на виртуальной машине. 

Использование команды "vagrant halt" для выключения виртуальных машин созданных с помощью Vargrant.

![Нажми сюда](images/14_report.png)

Выключенные машины.

Использование команды "vagrant destroy -f" для удаления виртуальных машин.

![Нажми сюда](https://disk.yandex.ru/i/grca747HXPSE9g)

Отсутствие машины.