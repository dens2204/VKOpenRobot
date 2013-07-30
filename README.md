VK Open Robot
==============

VK Open Robot - библиотека для создания ботов социальной сети VKontakte.

## Возможности ботов

1. Массовое добавление пользователей в друзья
2. Массовое вступление в группы
3. Массовая отправка сообщений на стены групп
4. Поиск групп
5. Поиск пользователей в группах
6. Получение развернутой информации о пользователе
7. Загрузка картинок на сервер VK, которые в дальнейшем могут быть вложены в сообщения на стены
8. Выставление статуса пользователя

## Компоненты API

* [VKConnector](docs/VKConnector.md) - фасад для вызова методов официального API VK

* [TokenProvider](docs/TokenProvider.md) - поставщик токенов пользователей, от имени которых работают боты

* [CaptchaParser](docs/CaptchaParser.md) - интерфейс парсера капчей

* [AntigateCaptchaParser](docs/AntiGateCaptchaParser.md) - реализация парсера капчей через сервис Antigate

* [VKBot](docs/VKBot.md) - реализация бота, который выполняет различные задачи

* [VKBotTask](docs/VKBotTask.md) - интерфейс задачи для бота

* [FriendInviteTask](docs/FriendInviteTask.md) - реализация VKBotTask для отправки предложения дружбы пользователю

* [GroupWallPostTask](docs/GroupWallPostTask.md) - реализация VKBotTask для отправки сообщения на стену группы


## Примеры:

* [FriendInviteBot](docs/FriendInviteBot.md) - робот для поиска групп по ключевому слову, выбора пользователей старше 18 лет,
проживающих в Москве или Санкт-Петербурге и отправки им предложения дружбы с текстом приветствия.
Текст приветствия содержит имя пользователя, кому адресуется и пользователя, от чьего имени работает робот.
Запуск: `mvn exec:java -P friend-invite-bot`

* [GroupWallPostBot](docs/GroupWallPost.md) - робот поиска групп по ключевому слову и отправки сообщений на стены найденных групп.
Сообщения включают в себя картинки и ссылки.
Запуск: `mvn exec:java -P group-wall-post-bot`