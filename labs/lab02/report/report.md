---
## Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Управление версиями"
author: "Артамонов Тимофей Евгеньевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

– Изучить идеологию и применение средств контроля версий.
– Освоить умения по работе с git.

# Задание

– Создать базовую конфигурацию для работы с git.
– Создать ключ SSH.
– Создать ключ PGP.
– Настроить подписи git.
– Зарегистрироваться на Github.
– Создать локальный каталог для выполнения заданий по предмету

# Теоретическое введение

Git - Система контроля версий (Version Control System, VCS) применяется при работе нескольких человек над одним проектом.
Ветвление - сохранение версий проекта для возможного последующего использования.
Хранилище - место, где хранятся все версии проекта.
commit - изменение в проекте.
Рабочая версия - версия проекта, над которой в данный момент ведется работа.
GitHub - веб-сервис, основанный на системе контроля версий Git.

# Выполнение лабораторной работы

## Настройка github
Регистрируем учётную запись github и заполняем основные данные. (рис.1)

![Профиль в GitHub](https://user-images.githubusercontent.com/104139992/165083905-8bbb4d0d-af23-4b30-aaf4-f008e72955eb.png){рис.1}

## Установка программного обеспечения

Устанавливаем git-flow в Fedora. (рис.2)

![Терминал](https://user-images.githubusercontent.com/104139992/165087838-e8086f2b-5ef4-4eb3-acfc-7a4efabf7225.png){рис.2}

Устанавливаем gh. (рис.3)

![Терминал](https://user-images.githubusercontent.com/104139992/165088051-b8673702-4c8d-4898-bb06-652596b81bfc.png){рис.3}

## Настройка git

Зададим имя и email владельца репозитория, то есть нас. (рис.4)

![Терминал](https://user-images.githubusercontent.com/104139992/165088290-2c10799f-c33a-4164-a764-c038e22f1b52.png){рис.4}

Зададим имя начальной ветки и параметры. (рис.5)

![Терминал](https://user-images.githubusercontent.com/104139992/165088774-67146e7d-3e62-4142-b585-c55472c0bd3c.png){рис.5}

## Создание ключей ssh и добавление их в GitHub

Создаем ed25519 ключ и точно так же rsa. (рис.6)

![Создание ssh ключей](https://user-images.githubusercontent.com/104139992/165088991-d55c9610-3c50-46e3-b996-a3f19449fbd4.png){рис.6}

Копируем ключи в буфер и по очереди добавляем их в гитхаб. (рис. 7, 8)

![Копирование ssh ключей](https://user-images.githubusercontent.com/104139992/165089151-cbe69a39-2a96-44d4-b213-4f81dd481503.png){рис.7}

![Вставка](https://user-images.githubusercontent.com/104139992/165089360-6aa354fa-8775-4a81-9cd9-4a2dd4439c0e.png){рис.8}

## Создание и добавление GPG ключа в GitHub

Создаём ключ и настраиваем его, так, как сказано в руководстве лабораторной работы. (рис.9)

![Создание ключа](https://user-images.githubusercontent.com/104139992/165089900-3f305160-a1cc-4e04-a5e0-0f76b37c4358.png){рис.9}

Указываем такой же адрес, как и на гитхабе. (рис.10)
 
![Указываем адрес](https://user-images.githubusercontent.com/104139992/165090066-9353e045-43d4-4e30-ad10-14c2ccc02ee5.png){рис.10}

Получаем отпечаток нашего ключа. (рис. 11, 12, 13)
 
![Привязываем ключ](https://user-images.githubusercontent.com/104139992/165090193-2d81f3f7-4145-40fc-9480-097a7fe5cc78.png){рис.11}
![ID ключа](https://user-images.githubusercontent.com/104139992/165090210-003c2e36-d384-4dd0-98dd-b3936c795fc3.png){рис.12}
![Отпечаток](https://user-images.githubusercontent.com/104139992/165090525-eb4be045-1eed-49e0-abca-aa2e80c4efd0.png){рис.13}

Копируем его в буфер. (рис.14)
 
![Копирование](https://user-images.githubusercontent.com/104139992/165090654-5b7b94ff-af5b-40bc-8516-994ce294303f.png){рис.14}

Добавляем его в гитхаб. (рис.15)

![Вставка](https://user-images.githubusercontent.com/104139992/165090872-d4e930c9-c88f-43b2-a278-989d3a544e2c.png){рис.15}

## Настройка автоматических подписей коммитов git
 
Настраиваем автоматические подписи с помощью нашей почты. (рис.16)

![Подписание](https://user-images.githubusercontent.com/104139992/165091076-d5bf2319-32b8-4616-9b53-fb1c80735df1.png){рис.16}

## Настройка gh

Входим в гитхаб через гит. (рис.17)

![Связывание](https://user-images.githubusercontent.com/104139992/165091225-80b1775c-f0a7-4686-8728-580a16d6097d.png){рис.17}

## Шаблон для рабочего пространства
 
Создаем папку. (рис.18)

![Создание](https://user-images.githubusercontent.com/104139992/165091693-34f628a0-40c2-45c4-a430-e17b8849d00f.png){рис.18}

Копируем шаблон. (рис.19)
 
![Копирование](https://user-images.githubusercontent.com/104139992/165091732-f883d86c-df4a-48ad-adb2-2a23648a9b31.png){рис.19}

Удаляем лишние файлы и создаем необходимые папки. (рис. 20, 21)
 
![Удаление](https://user-images.githubusercontent.com/104139992/165091858-77579f69-45cf-4275-a6d4-93579e6471b0.png){рис.20}
![Создание](https://user-images.githubusercontent.com/104139992/165091881-8ce79964-712d-4e3c-9624-b9148f19d359.png){рис.21}

Отправляем файлы на сервер. (рис. 22, 23)

![Отправка](https://user-images.githubusercontent.com/104139992/165091990-1f8be1f2-ab62-4fd8-9b86-69aff7fa0eef.png){рис.22}
![Отправка](https://user-images.githubusercontent.com/104139992/165092025-8996a9ee-a7a5-475f-852b-cf90095697f7.png){рис.23}

# Контрольные вопросы
1. Системы контроля версий (Version Control System, VCS) применяются при работе нескольких человек над одним проектом.
2. Хранилище - место в репозитории, где размещаюся все версии проекта и прочее.
Под commit понимается новая версия/изменения проекта.
История - список всех версий.
Рабочая копия - версия проекта, на которой в данный момент ведется работа.
Все эти явления связаны между собой и вместе представляют собой git.
3. Централизованная vcs – vcs с единым репозиторием. Примером может выступать репозиторий отдела баланса в видеоиграх.
Децентрализованная vcs – vcs с несколькими репозиториями. Пример - если участники не работают над одним проектом, например учебная группа в ВУЗе.
4. Человек просто работает с файлом и создает для него различные версии, возвращаясь после к лучшей из конкурентов и продолжает работать уже над ней.
5. С общим хранилищем, участники могут предлагать свои идеи по усовершенствованию файла, удачные добавляются и становятся частью нового файла.
6. Такие же как и у всех VCS.
7. Создание основной ветки git init 
получение обновлений текущего дерева из центрального репозитория git pull
отправка всех произведённых изменений локального дерева в центральный репозиторий git push
просмотр списка изменённых файлов в текущей директории git status
просмотр текущих изменения git diff
добавить все изменённые и/или созданные файлы и/или каталоги git add . 
добавить конкретные изменённые и/или созданные файлы и/или каталоги git add имена_файлов
удалить файл и/или каталог из индекса репозитория (при этом файл и/или каталог остаётся в локальной директории) git rm имена_файлов
сохранить все добавленные изменения и все изменённые файлы git commit -am 'Описание коммита' – сохранить добавленные изменения с внесением комментария git commit
создание новой ветки, базирующейся на текущей git checkout -b имя_ветки переключение на некоторую ветку git checkout имя_ветки (при переключении на ветку, которой ещё нет в локальном репозитории, она будет создана и связана с удалённой) 
отправка изменений конкретной ветки в центральный репозиторий git push origin имя_ветки 
слияние ветки с текущим деревом git merge --no-ff имя_ветки 
Удаление локальной уже слитой с основным деревом ветки git branch -d имя_ветки
Принудительное удаление локальной ветки  git branch -D имя_ветки – 
Удаление ветки с центрального репозитория git push origin :имя_ветки
8. - git add .
   - git rm
9. Ветки нужны для возможного отката версии или же просто для будущего выбора между ними нового ядра проекта.
10.  Некоторые файлы это файлы, генерируемые машиной для работы и как правило они не принимают прямого участия в разработке.


# Выводы

Создали свой репозиторий в git, создали аккаунт в github, связали git и github, научились пользоваться репозиторием и загрузили в хранилище отчёты и презентации.

# Список литературы

- Мой мозг
- Мой разум
- Моё сознание
- https://esystem.rudn.ru/pluginfile.php/1383169/mod_resource/content/4/002-lab_vcs.pdf
- https://esystem.rudn.ru/pluginfile.php/1383171/mod_resource/content/3/003-lab_markdown.pdf
