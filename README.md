# Самогонки / Moonshine Runners / Spanking Runners

(с) ООО "КД ВИЖЕН" (Калининград)

Весь код, за исключением сторонних библиотек, публикуется под лицензией GPLv3. Код сторонних библиотек (где указана иная лицензия) публикуется под лицензией этих библиотек.

Собранная игра совестима с официальным релизом с диска 1С.

Чат сообщества: https://t.me/SamogonkiGame

## Работоспособность кода

К сожалению, некоторые файлы кода были утеряны и заменены болванками. Их необходимо восстановить, анализируя остальной код. На данный момент оставшиеся проблемы:

* Музыка в формате MP+ не работает, вероятно нужно подключить для нее FFMPEG.
* Главное меню запускается, но похоже отображается в невидимом месте 3d-пространства, поэтому его не видно.
* Меню в игре также работают не полностью.
* ~~Не загружаются чекпоины на мирах~~ Исправлено
* Часть 3d-моделей визуализируются не полностью.
* Часть оружия может работать некорректно.

Исходный код, отвечающий за сайт samogonki.ru для веб-игр также не сохранился, но можно понять протокол по запросам.

## Состав репозитория

* MechoSoma - Основной исходный код
* stl, XLibsSpring2004 - библиотеки
* ParserDLL - Более новая версия aci_parser, можно переписать чтобы использовать не библиотеку.
* MSDXSDK_02_06 - DirectX SDK используемый игрой

Утилиты parser, который преобразует скрипты (scr) в бинарные скрипты (scb) нет, но ее можно восстановить, просто запуская команды parseScript/saveScript. Скрипты можно вообще не собирать пока.

## Пошаговая инструкция по сборке

Открываем в `VS2008` `MechoSoma\MechoSoma.sln`. Делаем Rebuild

## Что потребуется

Проверено что игра собирается в окружении Windows XP / Windows 7 / Windows 10 + Visual Studio 2008. Кроме того потребуется
установить Windows SDK 7.1 для воспроизведения видео, скачать можно по ссылке:

https://developer.microsoft.com/ru-ru/windows/downloads/sdk-archive/

В самом низу есть версия для Windows 7 и Windows XP (на Windows 10 он тоже подойдет).

## Запуск игры
* В game.ini установите show_images=0, resources=0
* Распакуйте все resource.pak файлы
* Скопируйте файл GameDBG в папку с игрой.

Игра запускается командой `gamedbg /W7-0 /skipmenu`. Это позволяет сразу попасть в мир-лобби.

Мир, в котором игра точно работает - Аллея Светлячков
