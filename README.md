# Homework_12-02

## Задание 1

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

<img width="974" height="478" alt="изображение" src="https://github.com/user-attachments/assets/5e45bdb2-7689-444d-8a36-ba50a25e91d4" />

<img width="974" height="409" alt="изображение" src="https://github.com/user-attachments/assets/eacd0aff-fda1-4e6c-ab64-9d71d141e760" />


1.2. Создайте учётную запись sys_temp.

<img width="974" height="75" alt="изображение" src="https://github.com/user-attachments/assets/7e19a712-5ad4-4097-ab47-ec475bdd7e3d" />

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

<img width="974" height="522" alt="изображение" src="https://github.com/user-attachments/assets/0cafed60-6b77-4e19-929a-2efd71a73dcf" />

1.4. Дайте все права для пользователя sys_temp.

<img width="974" height="191" alt="изображение" src="https://github.com/user-attachments/assets/8ae548df-c005-4720-968a-9104b13cd3a5" />

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

<img width="974" height="433" alt="изображение" src="https://github.com/user-attachments/assets/76e79ff7-fb53-4798-950a-de7ec7492ba8" />

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

<img width="974" height="165" alt="изображение" src="https://github.com/user-attachments/assets/2c85c05d-1842-45b5-9ab5-f42c6900f394" />

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

<img width="974" height="270" alt="изображение" src="https://github.com/user-attachments/assets/1e317d6a-0126-4bea-87ee-249ff33e51b0" />

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

<img width="785" height="1518" alt="изображение" src="https://github.com/user-attachments/assets/504e8655-a534-4668-9cd7-0652c53679fe" />

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

### Простыня с запросами

#### 1.2
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'secure_password';

#### 1.3
SELECT User, Host FROM mysql.user;

#### 1.4
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;

#### 1.5
SHOW GRANTS FOR 'sys_temp'@'localhost';

#### 1.6 (смена аутентификации)
ALTER USER 'sys_temp'@'localhost' IDENTIFIED WITH mysql_native_password BY 'secure_password';
FLUSH PRIVILEGES;

## Задание 2

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id

### Решение:

<img width="974" height="906" alt="изображение" src="https://github.com/user-attachments/assets/36970130-c27c-44c2-b93f-118c60e06065" />
