# Generator_bunker_tgbot

Предисловие: на создание бота как и самого генератора меня вдохновило отсутствие моего учителя целую неделю. Все эти уроки мы играли в бункер. Все карточки и катастрофы мы брали в интернете, но там они очень часто повторялись и кое-кто никак не мог открыть нужный сайт. И вот я решил сделать свой генератор, дополнив множество параметров. А также для меня это неплохой способ получше узнать про тг ботов.

1. Все импорты:
import telebot
from telebot import types
from random import choice
from random import randint
from copy import copy
import emoji
import settings

как видно использованы такие дополнительные библиотеки как choice, randint (само собой для рандома), copy (для копирования списков), emoji (чтобы все выглядело по феншую) и settings (для сохранности API бота).

2. Данные
Вы можете безопасно пополнять почти все характеристики людей, за исключением стажа. Переменная стажа не используется в коде, а является лишь памяткой, сам стаж генерируется взависимости от возраста игрока.
Также не стоит добавлять новые катастрофы без обновления генератора этих катастроф.

3. Генераторы и функции
Я думаю, что останавливаться на функциях генератора не стоит. Там идет про сравнение данных и последующий их возврат.
Если же смотреть на функцию gen_pers то уже стоит обратить внимание на использование safe переменных и функцию choice. Safe перемен. нужны для предотвращения повтора данных.

4. Ошибки в боте
Здесь организована проверка на введение корректных числовых данных, но нет ограничения на запрос. При этом если бот поймает ошибку этого запроса, то продолжит работать.

5. Отправка данных пользователю
Бот отправляет вам персонажа, если его еще не получил кто-то другой. Присутствует множество смайликов, их можно менять на свой вкус. Если персонажей не осталось, нужно ждать новую игру.

6. Как пользоваться
Правила использования содержатся в функции helpa, но если более подробно, то вот.
Один человек, он же хост, нажимает на кнопку создания комнаты и указывает количество играющих. Бот отправляет код от нее, и хост сообщает этот код всем играющим. Игроки нажимают на кнопку присоединения и вводят код. каждому из них присылается их личный персонаж. Игра начинается.
