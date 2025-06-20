---
title: "Знакомство с LaTeX"
collection: guide
permalink: /guide/Latex
excerpt: #'This paper is about the number 1. The number 2 is left for future work.'
venue: #'Journal 1'
---
**Шаблон отчета, курсовой и дипломной работы, созданный для студентов ИИТММ, ННГУ:** [download](https://github.com/forodie/forodie.github.io/raw/main/files/VKR.zip) [upd 28.01.2024]  

В случае компиляции в pdfLatex:
1. Раскомментировать следующие две строки в файле с преамбулой:  
```
\usepackage[T2A]{fontenc}
\usepackage[utf8]{inputenc}
```
2. Закомментировать следующие:  
```
\usepackage{fontspec}
\setmainfont{Times New Roman}
```  

В случае компиляции LuaLatex сделать иначе.  

## LaTeX --- это?
LaTeX (произносится как <<латех>>) --- инструмент для создания профессиональных документов, система набора и вёрстки. Используется для создания научных документов, статей, книг и других публикаций. Пользуясь этой системой, можно сосредоточиться только над содержимым документа, всё форматирование программа возьмёт на себя с учетом стилевого файла и установленной преамбулы (настройками). 

В текст легко встраиваются таблицы, картинки, код и, самое главное, математические формулы, что делает выбор LaTeX более предпочтительным при написании отчетов, курсовых работ и диплома.

Остальные аргументы в пользу LaTeX и его преимуществ можно изучить отдельно: статьи на хабре и других ресурсах или, посерьезнее, в книжках. Ссылки на некоторый полезный материал будут приведены в конце этого гайда.

## Установка LaTeX
Установка состоит из двух этапов:
- Выбор дистрибутива.
- Выбор редактора для работы с tex файлами.

Популярные дистрибутивы: MikTeX, TeX Live.

Популярные редакторы: TeX Studio, TeXworks, TeXnic, vscode (с расширением <<LaTeX Workshop>>).

Попробовать можно онлайн на overleaf.com

Начнем установку:
1. Под Windows/Mac обычно ставят [MikTeX](https://miktex.org/download), под Linux [TeX Live](https://www.tug.org/texlive/), под Mac [MacTeX](https://www.tug.org/texlive/). На сайтах представлен способ установки через консоль и обычным образом.
2. Редактор можно выбрать любой, но советую [TeX Studio](https://www.texstudio.org/) или в vscode с расширением <<LaTeX Workshops>> для более продвинутых. В данных редакторах для удобства можно выбрать шаблоны, быстро находить специфические символы и обозначения, пользоваться сниппетами и другими гибкими настройками. 

Всё необходимое на текущий момент установлено. Можно проверить корректность установки. Для этого создается main.tex в отдельной папке, в котором прописывается следующее содержимое:

```
\documentclass[12pt]{article}
\begin{document}
Hello world!
$f(x) = x^2 + 1$ % math mode 
\end{document}
```

После компиляции должен выйти результат в виде PDF файла в правом окне и в папке. 

Для использования русского языка в файлах требуется настройка преамбулы. Подробнее об этом изучите сами в предложенных ссылках в конце этой страницы.

## Полезное к прочтению
1. [Learn LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
2. [Осваиваем LaTeX за 30 минут (на русском)](https://habr.com/ru/companies/ruvds/articles/574352/)
3. [Как я пишу конспекты по математике на LaTeX в Vim](https://habr.com/ru/articles/445066/)
4. [Львовский С. М. Набор и вёрстка в пакете LATEX. — 3-е изд. М.: МЦНМО, 2003.](https://old.mccme.ru//free-books//llang/newllang.pdf)
5. [LaTeX в примерах](http://www.ccas.ru/voron/download/voron05latex.pdf)
6. [detexify - поиск символов](https://detexify.kirelabs.org/classify.html)
