## Командный проект "VKinder"

Цель командного проекта — разработать программу-бота для взаимодействия с базами данных социальной сети. Бот будет предлагать различные варианты людей для знакомств в социальной сети ВКонтакте в виде диалога с пользователем.

Выполнение кода запускается из файла [main.py](https://github.com/NadezhdaLimanova/VKinder/blob/main/main.py)

Для успешного запуска бота необходимо заполнить: 

* [token.txt](https://github.com/NadezhdaLimanova/VKinder/blob/main/Bot/token.txt) - токен группы для бота, 
* [token_vk.txt](https://github.com/NadezhdaLimanova/VKinder/blob/main/Bot/token_vk.txt) - токен пользователя

Все необходимые связи находятся в файле [requirements.txt](https://github.com/NadezhdaLimanova/VKinder/blob/main/requirements.txt)


Проект состоит из двух частей: 

* разработанного бота с функциями парсинга [папка Bot](https://github.com/NadezhdaLimanova/VKinder/tree/main/Bot)
* базы данных, куда записывается информация о пользователях [папка BD](https://github.com/NadezhdaLimanova/VKinder/tree/main/BD)

Бот работает следующим образом:

1. После запуска приложения необходимо нажать кнопку "Начать" в чате или написать "привет". Бот напишет именное приветствие и предложит на выбор две кнопки: "Показать анкеты" или "Показать избранное".
2. При нажатии на кнопку "Показать анкеты", бот будет запрашивать Вконтакте информацию о пользователе, его имя, возраст, город и пол с помощью парсинга.
3. Если у пользователя не указан возраст или указан частично, то бот предложит ввести возраст вручную. Если у пользователя не указан город, то бот предложит ввести город вручную. Если пользователь ошибся при вводе города, бот выведет ошибку и предложит кнопку "Начать заново".
4. Если информация введена верно, бот выведет случайный аккаунт потенциального кандидата, подходящего по заданным критериям(возраст +- 5 лет от возраста пользователя, совпадение по городу и противоположный пол), также будет указана имя и фамилия кандитата и три фотографии с самым большим количеством лайков.
5. Если у случайно выбранного аккаунта меньше трех фотографий, бот выведет сообщение о том что фотографий мало и предложит кнопку "Начать заново".
6. После просмотра анкеты пользователь может выбрать добавить ли ему анкету в избранное, посмотреть избранное или посмотреть следующего кандидата. Для этого необходимо будет нажать одну из трех кнопок "Добавить в избранное", "Пропустить" и "Посмотреть избранное. При добавлении в избранное бот оповестит о том, что выбранный профиль будет добавлен в избранное и предложит кнопку "Вернуться".
7. При нажатии кнопки "Пропустить" бот предложит анкету следующего кандидата.
8. При нажатии кнопки "Посмотреть избранное" бот либо сообщит о том, что пользователь пока никого не добавил в избранное либо покажет выбранные пользователем профили.



 
