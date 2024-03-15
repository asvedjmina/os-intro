---
## Front matter
title: "Отчёт по по лабораторной работе №5"
subtitle: "Операционные системы"
author: "Ведьмина Александра Сергеевна"

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

Настройка рабочей среды с помощью менеджера паролей pass.

# Задание

1. Установить необходимое программное обеспечение.
2. Изучить принцип работы менеджера паролей pass.
3. Установить дополнительное программное обеспечение.

# Теоретическое введение

Менеджер паролей pass создан в рамках идеалогии Unix. В нём данные хранятся в файловой системе в виде каталогов и файлов. Файлы шифруются с помощью GPG-ключа.

Структура базы паролей может быть произвольной. Если необходимо использовать дополнительное программное обеспечение, семантику необходимо заложить в структуру базы паролей.

На данный момент существует 2 основных реализации: pass и gopass.

# Выполнение лабораторной работы

Устанавливаю gopass.

![Установка gopass](image/Screenshot from 2024-03-09 23-17-49.png){#fig:001 width=100%}

Устанавливаю менеджер паролей pass.

![Установка pass](image/Screenshot from 2024-03-09 23-18-01.png){#fig:002 width=100%}

Просматриваю список имеющихся ключей. Так как список пуст, создаю новый ключ.

![Создание ключа GPG](image/Screenshot from 2024-03-09 23-22-51.png){#fig:003 width=100%}

Инициализирую хранилище.

![Инициализация хранилища](image/Screenshot from 2024-03-09 23-24-10.png){#fig:004 width=100%}

Синхранизирую хранилище с git, создавая структуру git и задавая адрес репозитория на хостинге.

![Синхронизация с git](image/Screenshot from 2024-03-09 23-27-16.png){#fig:005 width=100%}

Добавляю browserpass в Chrome.

![Добавление browserpass](image/Screenshot from 2024-03-09 23-38-27.png){#fig:006 width=100%}

Скачиваю browserpass c помощью sudo apt.

![Установка browserpass](image/Screenshot from 2024-03-09 23-55-50.png){#fig:007 width=100%}

Устанавливаю дополнительное программное обеспечение.

![Установка dunst](image/Screenshot from 2024-03-10 00-08-04.png){#fig:008 width=100%}

![Установка fonts-awesome](image/Screenshot from 2024-03-10 00-09-49.png){#fig:009 width=100%}

![Установка powerline-fonts](image/Screenshot from 2024-03-10 00-12-44.png){#fig:010 width=100%}

![Установка light](image/Screenshot from 2024-03-10 00-13-13.png){#fig:011 width=100%}

![Установка swaylock](image/Screenshot from 2024-03-10 00-16-38.png){#fig:012 width=100%}

![Установка kitty](image/Screenshot from 2024-03-10 00-17-07.png){#fig:012 width=100%}

![Установка warbar swaybg](image/Screenshot from 2024-03-10 00-17-42.png){#fig:013 width=100%}

![Установка mpv](image/Screenshot from 2024-03-10 00-18-52.png){#fig:014 width=100%}

![Установка grim](image/Screenshot from 2024-03-10 00-19-11.png){#fig:015 width=100%}

Устанавливаю бинарный файл.

![Установка бинарного файла](image/Screenshot from 2024-03-10 00-35-11.png){#fig:016 width=100%}

Создаю свой репозиторий для конфигурационных файлов на основе шаблона.

![Создание репозитория](image/Screenshot from 2024-03-10 00-35-32.png){#fig:017 width=100%}

Инициализирую chezmoi с моим репозиторием dotfiles.

![Инициализация chezmoi](image/Screenshot from 2024-03-10 00-37-59.png){#fig:018 width=100%}

Запускаю chezmoi. Просматриваю внесённые им изменения.

![Запуск chezmoi](image/Screenshot from 2024-03-10 00-39-14.png){#fig:019 width=100%}

Сохраняю изменения.

# Выводы

В ходе лабораторной работы я освоила навыки использования менеджера паролей pass.
