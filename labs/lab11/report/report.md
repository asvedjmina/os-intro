---
## Front matter
title: "Отчёт по лабораторной работе №11"
subtitle: "операционные системы"
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs.

# Задание

1. Ознакомиться с теоретическим материалом.
2. Ознакомиться с редактором emacs.
3. Выполнить упражнения.
4. Ответить на контрольные вопросы.

# Теоретическое введение

Emacs представляет собой мощный экранный редактор текста, написанный на языке
высокого уровня Elisp.

Определение 1. Буфер — объект, представляющий какой-либо текст.
Буфер может содержать что угодно, например, результаты компиляции программы
или встроенные подсказки. Практически всё взаимодействие с пользователем, в том
числе интерактивное, происходит посредством буферов.

Определение 2. Фрейм соответствует окну в обычном понимании этого слова. Каждый
фрейм содержит область вывода и одно или несколько окон Emacs.

Определение 3. Окно — прямоугольная область фрейма, отображающая один из буферов.
Каждое окно имеет свою строку состояния, в которой выводится следующая информация: название буфера, его основной режим, изменялся ли текст буфера и как далеко вниз
по буферу расположен курсор. Каждый буфер находится только в одном из возможных
основных режимов. Существующие основные режимы включают режим Fundamental
(наименее специализированный), режим Text, режим Lisp, режим С, режим Texinfo
и другие. Под второстепенными режимами понимается список режимов, которые включены в данный момент в буфере выбранного окна.

Определение 4. Область вывода — одна или несколько строк внизу фрейма, в которой
Emacs выводит различные сообщения, а также запрашивает подтверждения и дополнительную информацию от пользователя.

Определение 5. Минибуфер используется для ввода дополнительной информации и всегда отображается в области вывода.

Определение 6. Точка вставки — место вставки (удаления) данных в буфере

# Выполнение лабораторной работы

Открываю emacs.

![Открытие emacs](image/Screenshot from 2024-04-14 22-11-04.png){#fig:001 width=100%}

Создаю файл lab07.sh и вставляю в него предложенный текст.

![Создание lab07.sh](image/Screenshot from 2024-04-14 22-16-18.png){#fig:002 width=100%}

Сохраняю его. После вырезаю строку одной командой и вставляю её в конец файла.

![Перенос строки](image/Screenshot from 2024-04-14 22-18-37.png){#fig:003 width=100%}

Затем выделяю область текста и вставляю её в конец файла.

![Копирование области](image/Screenshot from 2024-04-14 22-19-47.png){#fig:004 width=100%}

Отменяю последнее действие.

![Отмена действия](image/Screenshot from 2024-04-14 22-19-54.png){#fig:005 width=100%}

Перенос курсора в начало строки.

![Курсор в начало](image/Screenshot from 2024-04-14 22-20-14.png){#fig:006 width=100%}

Перенос курсора в конец строки.

![Курсор в конец](image/Screenshot from 2024-04-14 22-20-21.png){#fig:007 width=100%}

Вывожу список активных буферов на экран.

![Вывод буферов](image/Screenshot from 2024-04-14 22-20-50.png){#fig:008 width=100%}

Делю фрейм на 4 части поэтапно.

![Экран на 4 части](image/Screenshot from 2024-04-14 22-22-50.png){#fig:009 width=100%}

Переключаюсь в режим поиска. Ищу слово "hello".

![Поиск слова](image/Screenshot from 2024-04-14 22-23-36.png){#fig:010 width=100%}

Перехожу в режим поиска строк по содержанию.

![Поиск строк](image/Screenshot from 2024-04-14 22-25-20.png){#fig:011 width=100%}

# Выводы

Я познакомилась с операционной системой Linux и получила практические навыки работы с редактором Emacs.

