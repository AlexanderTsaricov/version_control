# Подсказки по GIT

## Основное

Показать текущую версию GIT
```sh
git --version
```
Показать небольшой список команд GIT 
```sh
git
```
Указать имя программиста, которое будет привязываться к коммитам
```sh
git config --global user.name "Alexandr"
git config --local user.name "Alexandr"
```
Указать электронную почту, которая будет привязываться к коммитам
```sh
git config --global user.email "salispiligrim@yandex.ru"
git config --local user.email "salispiligrim@yandex.ru"
```
Удалить файл
```sh
rm Popa.txt
```
Переход к папке
```sh
cd c:\Desctop\Popa
```

### Создание репозитория

1. Переходим в рабочий каталог

```sh
cd <путь к каталогу>
```

2. Инициализируем GIT

```sh
git init
```

### Создание новой ветки
```sh
git branch <name new branch>
```
### Удаление ветки

```sh
git branch -d <branch name>
```

### Добавить файл в текущее сохранение

Добавляет файл "file" в текущее сохранение (текущюю фиксацию).
*Если после написания начала имени файла нажать tab на клавиатуре, то терминал автоматически добавит нужное имя файла*

```sh
git add <file>
```

### Сохранить (закоммитить)

Сохранит (закоммитит) текущие изменения, добавленные после последнего коммита

```sh
git commit -m "комментарий"
```

**После изменений файла, необходимо добавить эти изменения через git add "file"**

### Журнал коммитов

Выведет в терминал список текущих коммитов

#### Полная версия журнала

```sh
git log
```
Список коммитов (пример):
```sh
commit e17e240ba981a354b34fe13dd54291c9105ce5fe (HEAD -> master)
Author: Alexandr Vinokurov <salispiligrim@yandex.ru>
Date:   Fri Feb 23 16:05:56 2024 +0500

    add commit

commit e8fb184f7a1fc4ff921e62c87a4285d4e036b3c3
Author: Alexandr Vinokurov <salispiligrim@yandex.ru>
Date:   Fri Feb 23 15:56:51 2024 +0500
```

#### Сокращенная версия журнала

```sh
git log --oneline
```

Список коммитов (пример):
```sh
e17e240 (HEAD -> master) add commit
e8fb184 add create repository instr
e644d9b create file instruction git
b2a71d9 add link
6e91381 add link
```
#### Ключь graph

Ключ graph позволяет получить в терминал журнал коммитов в графическом варианте, где видны ветки и их слияние

```sh
git log --graph
```

## Переход (возврат) на нужный коммит

Переход на коммит по указанному хэшу
```sh
git checkout (b2a71d9 - "хэш коммита")
```
Переход на последний (актуальный) коммит
```sh
git checkout master
```

## Показать изменения

Показывает изменения между коммитами или по отношению к последнему коммиту

```sh
git diff
git diff e8fb184 b2a71d9
```

## Откат

Возврат изменений к последнему коммиту
```sh
git restore
```

## Отображение всех веток
```sh
git branch
```
## Переключение между ветками

```sh
git checkout <имя ветки>
```