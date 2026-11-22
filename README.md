# НИРС осень 2026

**Тема:** Проектирование защищённой системы машинного обучения с применением технологий многосторонних конфиденциальных вычислений.

Оформление — класс [BMSTU-IU8](https://ctan.org/pkg/bmstu-iu8) v1.9 (CatInCosmicSpace, MIT), опция `research` (отчёт о НИР, ГОСТ 7.32-2017 с поправками кафедры ИУ8).

## Структура

```
main.tex              каркас документа и данные титульного листа
main.bib              список источников (biblatex, стиль gost-numeric)
contents/             главы
  glossary.tex        термины и сокращения
  00-abstract.tex     реферат
  00-introduction.tex введение
  01-threats.tex … 06-trial-run.tex
  99-conclusion.tex   заключение
  A-appendices.tex    приложения
inc/                  изображения (bmstu.png нужен титульному листу)
BMSTU-IU8.cls, IU8-*.sty   класс шаблона (лежат в корне, чтобы находились в любом редакторе)
```

## Сборка

Нужен полный TeX Live (Prism, Overleaf, локальная установка):

```
latexmk -pdf main.tex        # pdfLaTeX + biber, настройки в .latexmkrc
```

или вручную: `pdflatex main` → `biber main` → `pdflatex main` ×2.

В Prism: Code → Download ZIP на GitHub → Import в Prism (загрузка .zip).
Компилятор — pdfLaTeX, библиография — biber.

## Что заменить перед сдачей

- данные титульного листа в `main.tex` (сейчас заглушки);
- текст глав (сейчас заготовки с пометкой `ЧЕРНОВИК`);
- конечные страницы русскоязычных источников в `main.bib`.
