# Инструкция по работе с git

## Что такое git? 

Git - это распределенная система котроля версий кода. Она нужна, чтобы контролировать распределенные команды, контролировать их изменения и управлять их работой. 

## Подготовка репозитория

Для того, чтобы создать репозиторий, используется команда *git init*. Для этого необходимо написать в терминале в папке будущего репозитория *git init*.

## Создание "сохранений"

Для того, чтобы созданить изменения и дальше сохранить их, необходимо внести изменения в окно изменений (Находится выше терминала). После этого сохранить написанный текст одним из двух способов:
1. нажать комбинацию клавищ Cntr S
2. нажать File - Save 

### Добавление файла к коммиту

Для добавления файла к коммиту используется команда *git add*. Пишется она следующим образом *git add <имя файла>* в терминале в папке с созданным репозитории.

### Создание коммита

Для создания нового "сохранения" используется команда *git commit*. Используется она следующим образом: в терминале с папкой-репозиторием пишется *git commit -m <Сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО** в ковычках (").

## Журнал изменений

Для просмотра журнала изменений используется команда *git log*. Для этого в терминале в папке репозитория достаточно написать *git log*.

## Перемещение между коммитами 

Для перемещения между сохранениями используется команда *git checkout*. Для того, чтобы переместиться на указанный коммит в терминале в папке с репозиториес пишем *git checkout <номер коммита>*. **Номер коммита** берется из журнала изменений, о котором сказанов выше. После перемещения на указанный коммит попадаем в состояние *detached head*. Чтобы вернуться в обычный режим, необходимо написать *git chechout master*.

## Ветки в git

## Слияние веток и разрешение конфликтов

Для того, чтобы слить ветки воедино необходимо проделать следующее: возвращаемся в необходимую ветку (ту ветку, *корневую ветку*, в которую будет вливаться вторая ветка), удостоверяется, что мы находимся в нужной ветки при помощи команды git branch. У нужной ветки будет стоять знак звёздочки (*). После этого вводим команду git merge название_вливаемой_ветки. Информация из вливаемой ветки поступает в корневую верку. 

Конфлик: в ходе вливания веток одной в другую может произойти конфликт изненений (наложение информации одной на другую или несовпадение имеющейся изначально, до изменений, информации). Такое проиходит в том случаи, когда после создания вливаемой ветки в корневой тоже вносились изменения. 
Существует 4 способа решения конфликта
* используется вариант корневой ветки
* используется вариант вливаемоей ветки
* используеются оба варианта
* происходит ручное форматирование

При выборе любого из вариантов необходима дополнительная ручная проверка (для избежания упущения информации).

## Удаление веток