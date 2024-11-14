# LR6
Лабораторная работа №6

# Отчет по лабораторной работе №6
## Тема: Система контроля версий

## Цель лабораторной работы
Изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и
удаленным репозиторием. 

## Порядок выполнения работы
В ходе выполнения работы были выполнены следующие шаги:

### Шаг 1: Создание аккаунта на GitHub
Зарегистрирован аккаунт на сайте GitHub.

### Шаг 2: Форк репозитория
Форкнут репозиторий с заданием: https://github.com/Yeetmq/LR6/tree/master

![[Pasted image 20241114223618.png]]
### Шаг 3: Установка Git
Установлен Git с сайта [https://git-scm.com/](https://git-scm.com/).

### Шаг 4: Настройка Git
Настроен клиент Git с помощью следующих команд:

```bash
git config --global user.name "Группа Фамилия И.О."
git config --global user.email "ваш_емейл@example.com"
```
![[Pasted image 20241114223658.png]]

### Шаг 5: Клонирование репозитория

```bash
git clone https://github.com/Kurtyanik/LR6
```
![[Pasted image 20241114223708.png]]

### Шаг 6: Добавление файла через GitHub и подтягивание изменений
Добавлен файл через веб-интерфейс GitHub и изменения подтянуты локально:

```bash
git pull
```
![[Pasted image 20241114223719.png]]

### Шаг 7: Получение истории операций
Получена история операций для каждой ветки:

```bash
git log --oneline --all
```
![[Pasted image 20241114223743.png]]

### Шаг 8: Просмотр последних изменений
Посмотрены последние изменения:

```bash
git log -p -1
```
![[Pasted image 20241114223757.png]]

### Шаг 9: Слияние ветки и разрешение конфликта
Создана и слита ветка feature в master, конфликтов не возникло:

```shell
git checkout -b feature
# Внесены изменения
git add .
git commit -m "Внес изменения в feature"
git checkout master
git merge feature
```
![[Pasted image 20241114224339.png]]
### Шаг 10: Удаление побочной ветки


Удалена ветка feature после слияния:

```shell
git branch -d feature
```

### Шаг 11: Сделаны несколько коммитов с комментариями

Внесены изменения в файл example.txt (поочерёдно добавил две строки) и сделаны коммиты:

```shell
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку(второй коммит).txt"
```
![[Pasted image 20241114224432.png]]
### Шаг 12: Откат коммита
Выполнен откат последнего коммита:

```shell
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку(второй коммит).txt"
```
![[Pasted image 20241114224459.png]]
### Шаг 13: Создание ветки для отчета

Создана ветка report для оформления отчета:
```shell
git branch report
git checkout report
```
![[Pasted image 20241114224521.png]]

### Лог команд
```# Настройка имени пользователя и email
git config --global user.name "4314 Паюнен Д.А."
git config --global user.email "denispajunen@mail.ru"

# Клонирование форкнутого репозитория
git clone https://github.com/Yeetmq/LR6/tree/master

# Переключение в директорию проекта
cd LR6

# Получение истории операций для всех веток
git log --oneline --all

# Просмотр последних изменений
git log -p -1

# Создание новой ветки
git branch feature

# Переключение на новую ветку
git checkout feature

# Внесение изменений, добавление их в индекс и коммит
git add example.txt
git commit -m ""Изменения в новой ветке"

# Переключение обратно на мастер и слияние веток
git checkout master
git merge feature

# Удаление побочной ветки после слияния
git branch -d feature

# Создание еще нескольких коммитов с комментариями
git add example.txt
git commit -m "Добавлена новая строка"
git add example.txt
git commit -m "Добавлена новая строка (второй коммит)"

# Откат последнего коммита
git revert HEAD

# Создание ветки для отчета и переключение на нее
git branch report
git checkout report

# Получение истории операций в отформатированном виде
git log --pretty=format:"%h %ad | %s%d [%an]" --date=short

# Отправка изменений на удаленный репозиторий
git push origin report
```