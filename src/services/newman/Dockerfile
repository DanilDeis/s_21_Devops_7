FROM node:alpine

# Устанавливаем newman
RUN npm install -g newman

# Устанавливаем bash
RUN apk add --no-cache bash

WORKDIR /etc/newman

# Копируем коллекцию внутрь образа
# COPY application_tests.postman_collection.json /etc/newman/

# Запускаем bash по умолчанию, чтобы контейнер не завершался сразу
ENTRYPOINT ["bash"]