Project1
========

Задания.
1 - Написать клиент серверное приложение. Включается в себе несколько развидностей. Начнем от простого к сложному: 
1.1 - Написать, используя сокеты клиента и сервер. Функционал: клиент может посылать сообщения серверу, сервер посылает в ответ клиенту сообщение, которое получил от него.
1.2 - Усложнение к предыдущему: добавить поддержку нескольких пользователей.
1.3 - Усложнение к предыдущему: каждый клиент должен иметь уникальное имя, которое укажет себе при старте программы. Если имя занято, то попросить клиента, выбрать другое.
1.4 - С помощью Qt реализовать простенький интерфейс для клиента. На нем должны быть следующие кнопки: подключиться, отправить сообщение, поле для ввода сообщения и ника пользователя.
1.5 - Усложнение к 1.4: добавить регистрацию пользователей на сервере. Сервер должен сохранять в xml зарегистрированного пользователя. Данные о пользователя произвольные, но должны быть обязательны: логин, пароль. Добавить авторизацию на сервере. Только после успешной авторизации пользователь может отправлять сообщения серверу.
1.6 - Усложнение к предыдущему: добавить возможность отправки сообщения от пользователя к пользователя. В интерфейсе должно быть поле с вводом логина пользователя, которому должно быть отправлено сообщение.
1.7 - Усложнение к предыдущему: добавить ники для пользователей. Усовершенствовать интерфейс, чтобы пользователь получал список онлайн пользователей, и мог выбрать с кем ему начать чат (как в скайпе например).
1.8 - Усложнение к предыдущему: вместо сохранения пользователей в xml файл, научиться работать с SqLite или SQL Compact, вести записи пользователей в базу данных.
1.9 - Усложнение к предыдущему: развернуть ms sql server express и перенести всю базу в него.

В идеале у вас должна получиться ICQ, только более простая. По ходу написания сталкнетесь со многоми вещами в программирование, получите хороший опыт. Итоговый функционал приложения:
1 - регистрация пользователя
2 - авторизация на сервере
3 - работа с базой данных
4 - получение списка онлайн пользователей (в идеале сделать систему "друзей" и видеть кто онлайн, а кто нет)
5 - отправка сообщений от пользователя к пользователю ( в идеале добавить передачу файлов)
6 - система статус - онлайн, занят, невидим, офлайн (если будет скучно;) для этого необходимо будет в базе данных держать отдельную таблицу, к которой будет содержаться текущее состояние пользователя, т.е. его статус. При авторизации, этот статус должен доставаться сервером из базы и отправляться пользователю в ответ)

Работаем по протоколу tcp\ip. Клиент и сервер держат постоянное подключение. Синхронные или асинхронные сокеты - на ваше усмотрение. (З.Ы. синхронные проще, но обязательно неблокирующие). Сервер должен быть многопоточным.