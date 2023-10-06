# Образ который качаем
FROM node:14.21.1-alpine

# Папка от корня где исполнять команды !!! Можно менять после команды
WORKDIR /app

# Команда копировать что - в папку
COPY package*.json ./

# исполнение команд в Shell format = прямая запись 
RUN npm install --silent 
RUN npm install react-scripts@5.0.1 -g --silent

# создание файла .dockerenv из из которого можно использовать переменные
ENV MY_NAME="John Doe"

# исполнение команды после создания контейнера
CMD ["nodemon", "--exec", "npm", "start"]
