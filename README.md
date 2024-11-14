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
![image](https://github.com/user-attachments/assets/9b68778d-5dcd-49a3-bf50-39c921b06144)


### Шаг 3: Установка Git
Установлен Git с сайта [https://git-scm.com/](https://git-scm.com/).

### Шаг 4: Настройка Git
Настроен клиент Git с помощью следующих команд:

```bash
git config --global user.name "Группа Фамилия И.О."
git config --global user.email "ваш_емейл@example.com"
```
![image](https://github.com/user-attachments/assets/ec222698-6b0e-4fe9-ae05-f4fdf58caec7)


### Шаг 5: Клонирование репозитория

```bash
git clone https://github.com/Kurtyanik/LR6
```
![image](https://github.com/user-attachments/assets/dcb9c33c-acca-4157-9157-5092c5ec3a4f)


### Шаг 6: Добавление файла через GitHub и подтягивание изменений
Добавлен файл через веб-интерфейс GitHub и изменения подтянуты локально:

```bash
git pull
```
![image](https://github.com/user-attachments/assets/e2ae9ec6-9ca1-4899-bf94-4acebaaca460)


### Шаг 7: Получение истории операций
Получена история операций для каждой ветки:

```bash
git log --oneline --all
```
![image](https://github.com/user-attachments/assets/2113c2a1-3aef-47c5-9519-859a665024ab)


### Шаг 8: Просмотр последних изменений
Посмотрены последние изменения:

```bash
git log -p -1
```
![image](https://github.com/user-attachments/assets/3ebec833-017f-4d08-bebd-1d8934d6f135)


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
![image](https://github.com/user-attachments/assets/95d665bb-41a7-4f1c-902d-13506823d7d0)

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
![image](https://github.com/user-attachments/assets/90deb616-9bc3-47ce-b3b8-2b08c36050d2)

### Шаг 12: Откат коммита
Выполнен откат последнего коммита:

```shell
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку(второй коммит).txt"
```
![image](https://github.com/user-attachments/assets/c7190dd4-1ce4-470a-bcdd-ee18503ddcc0)

### Шаг 13: Создание ветки для отчета

Создана ветка report для оформления отчета:
```shell
git branch report
git checkout report
```
![image](https://github.com/user-attachments/assets/4c017792-71b5-40a2-a634-9b88faaadc0b)



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
### Пояснение:
Этот лог команд показывает весь процесс выполнения лабораторной работы, включая настройку Git, создание веток, коммиты, слияние, откат коммитов и отправку изменений на GitHub.

## История операций
Получим и напечатаем историю операций. Сделаем это при помощи команды:

```shell
git log --pretty=format:"%h %ad | %s%d [%an]" --date=short
```

История операций: ![image](https://github.com/user-attachments/assets/c5bd5613-a7af-4bed-8a62-a285f92c5900)

## Вывод

В ходе выполнения лабораторной работы были изучены основные возможности системы контроля версий Git. Получены навыки работы с локальными и удаленными репозиториями, создания и слияния веток, разрешения конфликтов и оформления отчета в README.md файле.
