---
description: Все вопросы, которые касаются .tree формата и работы с ним.
---

# Что такое .tree?

<details>

<summary>Что такое .tree формат?</summary>

Tree формат - это специальный удобный формат текстовых данных, который ближе всего похож на json и yaml.\
Подробнее есть видео и статьи в этой презентации: [https://mol.hyoo.ru/#!author=nin-jin/repo=HabHub/article=37/section=slides/slides=https%3A%2F%2Fnin-jin.github.io%2Fslides%2Ftree%2F](https://mol.hyoo.ru/#!author=nin-jin/repo=HabHub/article=37/section=slides/slides=https%3A%2F%2Fnin-jin.github.io%2Fslides%2Ftree%2F)

</details>

<details>

<summary>Что такое x.view.tree файл в $mol?</summary>

Ссинтаксис по $mol view tree  [https://github.com/hyoo-ru/mam\_mol/tree/master/view#all-special-chars](https://github.com/hyoo-ru/mam\_mol/tree/master/view#all-special-chars) . Но в первый раз лучше прочитать её полностью, т.к. там есть примеры, как использовать в $mol.

<img src="../.gitbook/assets/image (3).png" alt="" data-size="original">

Файлы x.view.tree в модуле - это декларативный способ описать структуру страницы. Другими словами - это шаблонизатор на синтаксисе .tree.

Файл view.tree, сборщик компилирует в обычный класс на typescript.

Подробнее можете прочитать в этой статье [https://github.com/hyoo-ru/mam\_mol/tree/master/view](https://github.com/hyoo-ru/mam\_mol/tree/master/view#all-special-chars)

\
\
От комьюнити:\
\- Вы можете почитать view.tree на пальцах в этой статье [https://page.hyoo.ru/#!=pl2jnm\_cvgbaz](https://page.hyoo.ru/#!=pl2jnm\_cvgbaz)

</details>

<details>

<summary>Может ли работать модуль в $mol, без файла x.view.tree?</summary>

Да, x.view.tree - декларативное отображение структуры компоненто, но оно не обязательно. Модуль будет работать и без него

</details>

<details>

<summary>Где можно посмотреть x.view.tree вживую?</summary>

[Песочница для View.Tree](https://mol.hyoo.ru/#!Description=Setup%20your%20editor/author=nin-jin/repo=HabHub/article=13/slide=0/slides=https%3A%2F%2Fnin-jin.github.io%2Fslides%2Fslides%2F/section=view.tree)\
Вы можете зайти в неё и вживую посмотреть, в какой класс TS собирается view.tree&#x20;

</details>
