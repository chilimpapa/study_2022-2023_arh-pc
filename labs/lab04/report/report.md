---
## Front matter
title: "Отчета по лабораторной работе №4"
subtitle: "Архитектура вычислительных систем"
author: "Дмитрий Владимирович Орлюк"

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

Освоение процедуры компиляции и сборки программ, написанных на ассем-
блере NASM

# Задание

1. В каталоге ~/work/arch-pc/lab05 с помощью команды cp создайте копию
файла hello.asm с именем lab5.asm
2. С помощью любого текстового редактора внесите изменения в текст про-
граммы в файле lab5.asm так, чтобы вместо Hello world! на экран выво-
дилась строка с вашими фамилией и именем.
3. Оттранслируйте полученный текст программы lab5.asm в объектный
файл. Выполните компоновку объектного файла и запустите получивший-
ся исполняемый файл.
4. Скопируйте файлы hello.asm и lab5.asm в Ваш локальный репозиторий
в каталог ~/work/study/2022-2023/"Архитектура компьютера"/arch-
pc/labs/lab05/. Загрузите файлы на Github

# Выполнение лабораторной работы
1. Откроем терминал, создадим текстовый файл hello.asm, открыли этот файл с помощью команды gedit

![Создали текстовый файл, открыли](image/1.png){ #fig:001 with=90% }

2. Вставим данный в лабораторной работе текст.

![Вставка нужного текста](image/2.png){ #fig:002 with=90% }

3. Компилируем текст программы "Hello world!" с помощью команды nasm, проверяем, что файл был создан

![Компилируем текст команды](image/3.png){ #fig:003 with=90% }

4. Скомпилируем исходный файл hello.asm в obj.o

![Компиляция исходного файла](image/4.png){ #fig:004 with=90% }

5. Выполним команду ld -m elf_i386 obj.o -o main

![Выполнение команды](image/5.png){ #fig:005 width=90% }

6. Скопируем и переименуем файл hello.asm

![Копирование файла](image/6.png){ #fig:006 width=90% }

7. Внесем изменения в текст программы

![Внесение изменений в файл](image/7.png){ #fig:007 width=90% }

8. Запустим на выполнение созданный исполняемый файл (Не работает ни на одном компьютере, ничего не меняется, не знаю что с этим делать)

![Запуск файла](image/8.png){ #fig:008 width=90% }

# Выводы

Я освоил процедуру компиляции и собрки программ, написанный на ассемблере NASM, а также научился запускать на выполнение исполняемые файлы
