# 🚀 Telegram-бот "Орёл или Решка" с Docker, Zabbix и бэкапами

## 🔍 Описание проекта
**Бот для игры в "Орёл или Решку"**, развёрнутый на двух VPS (Teamweb) с:
- Резервным копированием (bash-скрипты + отдельный хост).
- Мониторингом через Zabbix (триггеры на проверку бэкапов).

---

## 📋 Инфраструктура
| Компонент          | Хост          | Назначение                     |
|--------------------|---------------|--------------------------------|
| **Бот**            | VPS #1        | Python + Docker                |
| **Бэкапы**         | VPS #2        | Хранение резервных копий       |
| **Zabbix Server**  | Локальный ПК  | Мониторинг хостов              |

---

## 🛠️ Установка и настройка
### 1. Подготовка хоста под бота
- Установка Python, pip, зависимостей.  
  ![Установка Python](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20%D1%81%20%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8F%D0%BC%D0%B8%20.png)  

### 2. Работа бота
- Пример игры в Telegram.  
  ![Бот в работе](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%20%D1%81%D0%B0%D0%BC%D0%BE%D0%B3%D0%BE%20%D0%B1%D0%BE%D1%82%D0%B0.png)  

### 3. Docker-развёртывание
- **Dockerfile** (основные инструкции):  
  ![Dockerfile](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%20%D0%B4%D0%BE%D0%BA%D0%B5%D1%80%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.png)  
- **docker-compose.yml** (запуск в контейнере):  
  ![Docker Compose](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%20docker-compose.png)  

---

## ⚠️ Безопасность
Скрипты и конфиги содержат чувствительные данные (IP-адреса, токены), поэтому:
- Исходный код скриптов **доступен для проверки на собеседовании**.
- В репозитории — только **скриншоты ключевых частей** (без данных).

---

## 🔄 Бэкапы
### 1. Пример скрипта создания бэкапа
![Backup Script](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/%D0%A1%D0%BA%D1%80%D0%B8%D0%BF%D1%82%20%D0%91%D1%8D%D0%BA%D0%B0%D0%BF%D0%B0.png)  
**Логика:**  
- Архивация данных бота.
- Автоматический перенос на резервный хост.

### 2. Проверка свежести бэкапов
![Check Freshness](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/%D0%A2%D1%80%D0%B8%D0%B3%D0%B3%D0%B5%D1%80%20%D0%BD%D0%B0%20%D1%81%D0%B2%D0%B5%D0%B6%D0%B5%D1%81%D1%82%D1%8C%20%D0%B1%D1%8D%D0%BA%D0%B0%D0%BF%D0%BE%D0%B2.png)  
**Интеграция с Zabbix:**  
- Триггер срабатывает, если бэкап не обновлялся >24 часов.

---

## 📊 Мониторинг (Zabbix)
### 1. Дашборд Zabbix
- Мониторинг состояния бота и бэкапов.  
  ![Zabbix Dashboard](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/Zabbix%20%D0%BD%D0%B0%20%D1%82%D1%80%D0%B5%D1%85%20%D1%85%D0%BE%D1%81%D1%82%D0%B0%D1%85.png)  

### 2. Настройка агента
![Zabbix Agent Config](https://github.com/Evgenii199130/my_proekt/blob/main/Screen/Zabbix%20%D1%85%D0%BE%D1%81%D1%82%D1%8B.png)  

---  


Ссылка на телеграмм бота t.me/HeadsTails13Bot
Мой телеграмм @Igan310
