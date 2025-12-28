# 🥭 Mango Server - Backend чата

Backend для real-time чата с приватными сообщениями и отслеживанием онлайн-статуса.

## 🚀 Быстрый старт

```bash
# Установка
npm install

# Запуск
npm run dev
# или
node server.js

GET /status
json
{
  "status": "OK",
  "usersOnline": 0,
  "message": "Mango Server работает!"
}

## ⚙️ Конфигурация
Порт: 3001 (или через PORT переменную окружения)

bash
PORT=4000 npm run dev

## 📊 Хранение данных
const onlineUsers = new Map(); // socket.id → {id, nickname, avatar}

## 🔗 Подключение
const socket = io('http://localhost:3001');

## 📋 Зависимости
json
{
  "express": "^4.18.2",
  "socket.io": "^4.7.2",
  "cors": "^2.8.5"
}