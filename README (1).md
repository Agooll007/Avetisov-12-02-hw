# Домашнее задание к занятию «8.3. GitLab» - `Аветисов Николай`

---

### Задание 1

**Что нужно сделать:**

Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
![alt text]
1.2. Создайте учётную запись sys_temp.

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)
![alt text]

1.4. Дайте все права для пользователя sys_temp.

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
![alt text]

1.6. Переподключитесь к базе данных от имени sys_temp.


Для смены типа аутентификации с sha2 используйте запрос:
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
![alt text]

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

Простыня со всеми запросами:

SELECT VERSION();

CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'TempPass123!';

SELECT user, host FROM mysql.user;

GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;

SHOW GRANTS FOR 'sys_temp'@'localhost';

ALTER USER 'sys_temp'@'localhost'
IDENTIFIED WITH mysql_native_password
BY 'TempPass123!';

SELECT user, host, plugin FROM mysql.user WHERE user='sys_temp';

CREATE DATABASE sakila;

USE sakila;
SHOW TABLES;

---

### Задание 2

**Что нужно сделать:**

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id

![alt text](https://github.com/Agooll007/Avetisov_nikolay-8.3-GitLab-hw/blob/main/skrin2.png)
