# Шаг 1: Берем официальный и легкий образ веб-сервера Nginx
FROM nginx:stable-alpine

# Шаг 2: Удаляем стандартную страницу Nginx, которая идет по умолчанию
RUN rm -rf /usr/share/nginx/html/*

# Шаг 3: Копируем наш index.html (и будущие файлы) в папку, откуда Nginx раздает статику
COPY . /usr/share/nginx/html

# Шаг 4: Открываем стандартный HTTP-порт 80 для доступа извне
EXPOSE 80

# Шаг 5: Запускаем Nginx внутри контейнера
CMD ["nginx", "-g", "daemon off;"]
