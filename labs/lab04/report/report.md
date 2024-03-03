---
## Front matter
title: "Отчёт по лабораторной работе №4"
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

Получение навыков правильной работы с репозиториями git.

# Задание

1. Ознакомиться с теоретическим введением в git flow.
2. Создать учебный репозиторий.
3. Сделать несколько релизов.

# Теоретическое введение

Gitflow Workflow опубликована и популяризована Винсентом Дриссеном. Она предполагает выстраивание строгой модели ветвления с учётом выпуска проекта и отлично подходит для организации рабочего процесса на основе релизов.

Модель Gitflow включает в себя следующую последовательность действий:

1. Из ветки master создаётся ветка develop.
2. Из ветки develop создаётся ветка release.
3. Из ветки develop создаются ветки feature.
4. Когда работа над веткой feature завершена, она сливается с веткой develop.
5. Когда работа над веткой релиза release завершена, она сливается в ветки develop и master.
6. Если в master обнаружена проблема, из master создаётся ветка hotfix.
7. Когда работа над веткой исправления hotfix завершена, она сливается в ветки develop и master.

# Выполнение лабораторной работы

Устанавливаю git-flow.

![Установка git-flow](image/Screenshot from 2024-03-03 16-36-56.png){#fig:001 width=100%}

Загружаю Node.js.

![Установка node.js](image/Screenshot from 2024-03-03 16-38-40.png){#fig:002 width=100%}

Устанавливаю программы для форматирования коммитов и создания логов.

![Установка доппрограмм](image/Screenshot from 2024-03-03 17-32-40.png){#fig:003 width=100%}

Создаю репозиторий git-extended. Делаю первый коммит и выкладываю на гитхаб.
![Первый коммит](image/Screenshot from 2024-03-03 16-50-44.png){#fig:004 width=100%}

Произвожу конфигурацию пакетов node.js.

![Конфигурация node.js](image/Screenshot from 2024-03-03 16-56-54.png){#fig:005 width=100%}

Заполняю название пакета и лицензию (CC-BY-4.0), теперь package.json выгялдит следующим образом

![Вид package.json](image/Screenshot from 2024-03-03 17-20-19.png){#fig:006 width=100%}

Добавляю новые файлы, выполняю коммит и отправляю всё на гитхаб.

![Отправка новых файлов на гитхаб](image/Screenshot from 2024-03-03 17-31-35.png){#fig:007 width=100%}

Инициализирую git-flow, загружаю весь репозиторий в хранилище.

![Инициализация git-flow](image/Screenshot from 2024-03-03 17-38-12.png){#fig:008 width=100%}

Создаю релиз с версией 1.0.0.

![Создание релиза 1.0.0](image/Screenshot from 2024-03-03 17-38-56.png){#fig:009 width=100%}

Создаю журнал изменений, добавляю его в индекс и заливаю релизную ветку в основную.

![Работа с журналом изменений](image/Screenshot from 2024-03-03 17-41-05.png){#fig:010 width=100%}

Отправляю все изменения на гитхаб.

![Отправка изменений на гитхаб](image/Screenshot from 2024-03-03 17-44-16.png){#fig:011 width=100%}

Создаю релиз 1.0.0 на гитхаб.

![Создание релиза 1.0.0 на гитхабе](image/Screenshot from 2024-03-03 17-44-38.png){#fig:012 width=100%}

Создаю ветку для новой функциональности, а после объединяю ветку feature с develop.

![Работа с веткой для новой функциональности](image/Screenshot from 2024-03-03 17-45-22.png){#fig:013 width=100%}

Создаю релиз с версией 1.2.3.

![Создание релиза 1.2.3](image/Screenshot from 2024-03-03 17-47-40.png){#fig:014 width=100%}

Обновляю номер версии в package.json.

![Обновление package.json](image/Screenshot from 2024-03-03 17-48-11.png){#fig:015 width=100%}

Создаю журнал изменений, добавляю его в индекс, после чего заливаю ветку в основную.

![Добавление ветки релиза 1.2.3 в основную](image/Screenshot from 2024-03-03 17-50-37.png){#fig:016 width=100%}

Отправляю всё на гитхаб.

![Отправка изменений на гитхаб](image/Screenshot from 2024-03-03 17-51-50.png){#fig:017 width=100%}

Загружаю релиз 1.2.3 на гитхаб.

![Создание релиза 1.2.3 на гитхабе](image/Screenshot from 2024-03-03 17-52-11.png){#fig:018 width=100%}

# Выводы

В ходе лабораторной работы я освоила навыки углубленной работы с репозиторием git.
