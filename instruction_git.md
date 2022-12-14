# **Инструкция по работе с Git**

![эмблема_гит](JPG.JPG)

## Предварительная настройка Git

Чтобы "предствиться" программе git нужно ввести команды:

    git config --global user.name "Ваше имя"
    git config --global user.email "Ваш e-маил"

## Создание репозитория

Чтобы инициализировать новый файл нужно ввести команду:

    git init
## Добавление в индекс

Чтобы добавить изменения в индекс (для фиксации в следующем коммите) нужно
ввести команду :

    git add <имя файла>

## Фиксация изменений

Чтобы зафиксировать изменения, добавленные в индекс нужно ввести команду:

    git commit

при этом откроется окно для краткого ввода комментария о коммите

Чтобы ввести комментарий, не открывая отделаьное окно, нужно использовать эту же команду, с дополнением:

    git commit -m "комментарий"

чтобы автоматически индексировать изменения в файлах проекта, нужно использовать другое дополнение:

    git commit -a

Чтобы создать коммит всех проиндексированных изменений и добавить к коммиту подставленный комментарий:

    git commit -am "комментарий"

## Просмотр истории коммитов

Чтобы посмотреть историю изменений коммитов используется команда:

    git log

Чтобы увидеть историю изменений в кратком виде, нужно добавить в команду опцию:

    git log --oneline

Чтобы увидеть все изменения, независимо от того на какой коммит, мы сейчас переключены, используется таже команда с другим добавлением:

    git log --all

Чтобы увидеть все изменения, независимо от того на какой коммит, мы сейчас переключены, в кратком виде, используется команда:

    git log  --all --oneline

## Просмотр различий между коммитами

Для просмотра различий между разными версиями репозитория используется команда:

    git diff <номер одного коммита> <номер другого коммита>

При этом если ввести команду 

    git diff

без параметров - будет показана разница между текущим состоянием репозитория и последним который мы коммитили.

# Переключение между коммитами

Чтобы переключиться с коммита на котором вы находитесь, на любой другой, нужно ввести команду:

    git checkout номер коммита

Чтобы вернуться в нормальный рабочий режим с коммитами, из переключенного, нужно ввести команду

    git checkout master

## Проверка состояния репозитория

Чтобы проверить состояние репозитория необходимо ввести команду: 

    git status

## Ветвеления

Ветвления в Гит нужны для того, чтобы можно было контролировать работу, когда работают несколько человек, над одним проектом.

## Создание новой ветки
Чтобы создать новую ветку, используется команда:

    git branch название

## Просмотр всех веток
Чтобы посмотреть существующие ветки и на какой из них вы находитесь, используется команда:

    git branch

## Слияние веток

Чтобы влить одну ветку в другую необходимо находясь в ветке, в которую будем вливать другую, использовать команду:

    git merge название_вливаемой_ветки

## Удаление веток

Чтобы удалить ненужную ветку, используется команда:

    git branch -d имя_удаляемой_ветки

## Переход между ветками

    git checkout
## Переключение между ветками

Чтобы переключаться между разными ветвями используется команда:

    git checkout название_ветки_на_которую_переключаются

## Конфликты при слиянии веток

Если одна и та же строка в разных ветках при слиянии заполнена, возникнет конфликт при слиянии подобных веток.
Сама программа гит, не использующая другие программы, выводит оба изменения при слиянии, далее нужно вручную внести нужные правки и сделать commit.

Visual Studio Code позволяет выбрать какие изменения из слитых веток сохранить, или дает выбор сохранить оба изменения.

## Удаленные репозитории

Чтобы создать удаленный репозиторий, нужно на сайте github.com создать аккаунт, в аккаунте создать репозиторий, далее нужно будет ввеси следующие команды:

    git remote add origin ссылка репозитория (пример: https://github.com/DamnumAX/Seminar-3.git)

    git branch -M (main или master) - создает ветку в удаленном репозитории на сайте, поэтому "-M" должна быть большой, чтобы не запутаться также следует называть ветку, соответственно главной ветке, в вашем файле.

    git push -u origin (main или master) - пушит репозиторий в первый раз на сайт гитхаб

Чтобы обновить информацию репозитория после его создания, нужно использовать команду 
   
    git push
    
Чтобы перенести изменения из удвленного репозитория в обычный рабочий репозиторий, нужно ввести команду:

    git pull
