**План тестирования возможности записаться на обучение профессии «Тестировщик ПО"**


**1.Перечень автоматизируемых сценариев**

*Сценарии навигации к форме для записи на обучение профессии "Тестировщик ПО"*

1 сценарий. Зайти на начальную страницу https://netology.ru/ , нажать на меню "Каталог курсов", слева выбрать "Программирование", из всплывающего перечня профессий выбрать "Тестировщик ПО", осуществится переход на страницу https://netology.ru/programs/qa. 

2 сценарий. Зайти на начальную страницу https://netology.ru/ , найти подзаголовок "Направления обучения" и выбрать "Программирование", осуществится переход на страницу https://netology.ru/development, нажать на  "Тестировщик ПО" (первая в списке профессия), осуществится переход на страницу https://netology.ru/programs/qa. 

*Способы записи на обучение*

Перейдя на страницу професии "Тестировщик ПО" https://netology.ru/programs/qa, записаться на обучение можно тремя способами:

1 способ. В начале страницы слева зеленая кнопка "Записаться".

2 способ. Начать пролистывать вниз и сверху справа (рядом с кнопкой "Войти") появится голубая кнопка "Записаться".

3 способ. Пролистать всю страницу профессии вниз до формы записи.


*API тестирование*

-Позитивные проверки

Проверка поддержки MySQL
Проверка поддержки Postgres
Проверка корректности данных записанных в БД


*UI тестирование*

*Перечень сценариев заполнения и отправки формы записи*

Позитивное тестирование:

1. Ввести валидное имя на кириллице в поле Имя ( Анна)

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

Ожидаемый результат - Появляется сообщение об успешной отправки заявки


Негативное тестирование (1):

1. Ввести невалидное значение (спецсимволы) в поле Имя (@#$%^&*!"№;%:?)

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя не может содержать спец символы


Негативное тестирование (2):

1. Ввести пробел в поле Имя 

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некоректно


Негативное тестирование (3):

1. Ввести невалидное имя на латинице в поле Имя ( Andrey)

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некоректно


 Негативное тестирование (4):

1. Ввести невалидное имя, состоящее из 1 буквы на кириллице (А)

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некоректно


 Негативное тестирование (5):

1. Оставить поле Имя пустым

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя должно быть заполнено


  Негативное тестирование (6):

1. Ввести невалидное имя, состоящее из цифр (32665663)

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некоректно


Негативное тестирование (7):

1. Ввести невалидное имя, состоящее из 60 букв на латинице 

2. Ввести валидный номер телефона из 11 цифр (79774440022)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некоректно


Негативное тестирование (8):

1. Ввести валидное имя на кириллице в поле Имя ( Анна)

2. Ввести невалидный номер телефона из 1 цифры (7)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон заполнено некоректно


Негативное тестирование (9):

1. Ввести валидное имя на кириллице в поле Имя ( Анна)

2. Ввести невалидный номер телефона из 15 цифр (79771234567894)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон заполнено некоректно
 

Негативное тестирование (10):

1. Ввести валидное имя на кириллице в поле Имя ( Анна)

2. Ввести буквы кириллицы в поле Телефон (рлуооадлвд)

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон заполнено некоректно


Негативное тестирование (11):

1. Ввести валидное имя на кириллице в поле Имя ( Анна)

2. Поле Телефон оставить пустым

3. Нажать на копку Записаться 

 Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон должно быть заполнено



**2.Перечень используемых инструментов с обоснованием выбора.**

-IDEA - платформа для удобного написание кода и тестов

-Gradle - система для установки различных зависимостей 

-JUnit - библиотека, для написания автотестов

-CI - система непрерывной интеграции, позволяет отслеживать наличие ошибок, чтобы сборка не упала

-Docker - программа для установки различных баз данных

-Selenide - фреймворк для автоматизированного тестирования, для работы с селекторами

-Git и Github - Система контроля версий, для хранения кодов автотестов

-Faker - генерация случайных тестовых данных

-Jira- инструмент для создания баг-репортов.


**3.Перечень необходимых разрешений, данных и доступов.**

При выполнении автоматизированного тестирования сайта необходимо получить разрешение на выполнение таких работ у владельца сайта.

Необходим доступ к БД, чтобы проверить отправилась ли заявка.

Доступ к API для тестирования через API

**4.Перечень и описание возможных рисков при автоматизации.**

Риск появления проблем с настройкой тестирования, соответствующего окружения и подключения к БД

Т.к сайт сложный, могут возникнуть сложности с поиском элементов на странице (отсутствие тестовых меток).

**5.Перечень необходимых специалистов для автоматизации.**

QA-engineer 

Тестировшик 

**6.Интервальная оценка с учётом рисков в часах.**

Подготовка окружения, развертывание БД - 12 часов.

Написание автотестов, тестирование и отладка автотестов - 24 часа.

Формирование и анализ отчетов - 6 часов.