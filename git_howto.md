# Шпаргалка по GIT
## Инициализация нового репозитория
```sh
git init
```
## Получить информацию от GIT о его текущем статусе

```sh
git status
```

## Добавить файл или файлы к следубщему коммиту

```sh
git add
```

## Создание коммита
```sh
git commit -m "message"
```
## Если закоммитить без коммента
>Открывается редактор VIM (актуально для Windows). См. VIM tips в отдельном файле




## Вывод на экран истории всех коммитов с их хеш-кодами

```sh
git log
```

> При добавлении достаточно большого количества коммитов, показывается сокращённый список, который можно скроллить стрелками. Для выхода из режима просмотра списка, press **q**

![git log.png](.\images\git_log.png)

Краткий список коммитов
```sh
git log --oneline --graph
```
![git log с короткой и графической записью.png](.\images\git_log_short.png)

## Переход от одного коммита к другому

``` sh
git checkout хэш-код
```
![git log.png](.\images\git_log.png)

> шестнадцатеричный хэш-код можно вводить не целиком, а только первые 4 символа

* маркер *HEAD* показывает, на каком коммите мы находимся
* маркер *master* показывает, что мы находимся в конце ветки, под названием "master". То есть последний коммит

Если  **HEAD -> master**, значит мы на последнем коммите

>Если маркера с названием ветки нет, значит мы в статусе **Detached head**
![безголовый гит лог.png](.\images\git_log_detached_head.png)

## Вернуться к актуальному состоянию и продолжить работу
```sh
git log master
```
## Увидеть разницу между текущим и закоммиченным состоянием

```sh
git dif
```
![git diff.png](.\images\git_diff.png)


## [Руководство по MarkDown](https://paulradzkov.com/2014/markdown_cheatsheet/) взято с [этого сайта](https://paulradzkov.com)

## Просмотреть все имеющиеся ветки

```sh
git branch
```

## Создать новую ветку

```sh
git branch branch_name
```

## Удалить ветку
```sh
git branch -d branch_name
```

## Перейти на другую ветку

```sh
git checkout branch_name
```

## Создать новую ветку и перейти на неё

```sh
git checkout -b branch_name
```

## Влить ветку branch_name в текущую

```sh
git merge branch_name
```

При возникновении конфликта (ошибка будет указана крупными буквами), редактируем файл, оставляя только нужное.
Затем - создаём новый коммит.

# Git Hub
## Существует два способа начать работу:

1. Закачать репозиторий с локального компьютера

В интерфейсе git hub это делается через создание нового репозитория:

![как создать новый репозиторий](.\images\gh_create_button.png)

Затем требуется выбрать параметры нового репозитория.

**Nota bene**: *если предполагается закачка не нового, а готового репозитория, не стоит ставить галочки для создания базовых файлов (readme, gitignore), ибо может возникнуть конфликт*

![варианты создания нового репозитория](.\images\gh_new_repo.png)
Далее видим удобную инструкцию с готовыми командами:
+ Для создания нового локального репозитория через командную строку и загрузки его на git hub
+ Для загрузки уже имеющегося репозитория
+ Для импорта кода из другого репозитрия (*это  мы не проходили, это нам не задавали*)

2. **Форкнуть** чей-то чужой проект, копия которого возникнет в списке твоих репозиториев.

## Дальнейшая работа с репозиторием

1. Можно конечно с ним работать прямо в интерфейсе git hub (но кажется, так никто не делает)    

