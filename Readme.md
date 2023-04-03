# Инструкция по работе с Git и удалёнными репозиториями

## Что такое git?
**Git** - это наиболее популярная реализация распределённой системы контроля версий. Самая популярная реализация **Git** - это [GitHub](https://github.com/)

## Подготовка репозитория
Для сооздания репозитория используется команда *git init*. Для этого необходимо в терминале перейти в пустую папку, где в будущем будет репозиторий. Затем в терминале с папкой написать команду *git init*.

## Создание коммитов

### Добавление файла к коммиту
Для добавления файла к будущему коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

### Создание коммита
Для создания коммита используется команда *git commit*. Для этого в терминале с папкой репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для перемещения на предущие коммиты используется команда *git checkout*. Для этого необходимо в журнале изменений, как показано в предыдущей части, найти необходимый коммит и его номер. После чего в терминале с папкой-репозиторием написать команду *git checkout <номер коммита>*. После примененения этой команды Вы попадёте в состояние **Detached head**, в котором никакие изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *git checkout master*.

## Ветки в Git
### Создание веток в Git
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*
### Просмотр списка веток
Для просмотра списка веток используется комнада *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*. Зелёным цветом с символом **звёздочка** будет выделена текущая ветка

### Переключение между вектами
Для перехода на другую ветку используется команда *git checkout*. Для этого в терминале с папкой-репозиторием пишем команду *git checkout <название ветки*. Для перехода на ветку ветка должна быть ***создана***!!!

## Слияние веток и разрешение конфликтов

## Удаление веток

## Работа с удаленными репозиториями
Удаленный репозиторий – это версии вашего проекта, сохраненные на удаленном сервере. Доступ к репозиторию на таком сервере может осуществляться по интернету или по локальной сети.
Удаленный репозиторий – полноценный репозиторий, ничем не отличающийся от локального. У удаленного репозитория есть собственные ветки,своя история коммитов и так далее.
Если мы подключим удаленный репозиторий к своему локальному, то у нас появятся копии всех ссылочных объектов удаленного репозитория.
__*Команды для работы с удаленными репозиториями*__:
   
1. **Связь локального и удаленного репозиториев. Команда git remote**.
   Необходимость подключить удаленный репозиторий к уже существующему локальному возникает в ситуациях, когда вы решаете выгрузить уже написанный код на удаленный сервер. Это нужно, чтобы другие разработчики смогли получить к нему доступ или чтобы вы сами могли заниматься разработкой с нескольких компьютеров (например, домашнего и рабочего).
   Чтобы добавить удаленный репозиторий к вашему локальному используется команда **_git remote add_**.
   
   _Формат_: **git remote add** <название удаленного репозитория> <ссылка на удаленный репозиторий>

   Название - принято называть удаленный репозиторий **origin**, но строго говоря, никаких ограничений здесь нет.

   Ссылка - URL адрес репозитория на GitHub.

   _Пример_:

   git remote add origin https://github.com//......
2. Клонирование удаленного репозитория. Команда git clone.
3. Получение изменений из удаленного репозитория. Команда git pull.
4. Отправка изменений в удаленный репозиторий. Команда git push.
5. Создание форка репозитория на GitHub. Пулл-реквесты.
