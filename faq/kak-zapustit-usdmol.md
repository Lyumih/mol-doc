---
description: Вопросы связанные с тем, чтобы просто запустить $mol в первый раз
---

# Как запустить $mol?

<details>

<summary>Как запустить $mol в браузере?</summary>

Самый быстрый способ попробовать $mol - это запустить его на GitPod. [https://gitpod.io/#https://github.com/hyoo-ru/mam](https://gitpod.io/#https://github.com/hyoo-ru/mam)

Подробнее тут: [https://mol.hyoo.ru/#!demo=mol\_button\_demo/bench=init/Description=Create%20MAM%20project](https://mol.hyoo.ru/#!demo=mol\_button\_demo/bench=init/Description=Create%20MAM%20project)

</details>

<details>

<summary>Как запустить $mol локально?</summary>

Нужно клонировать проект и запустить. Подробнее тут: [https://mol.hyoo.ru/#!demo=mol\_button\_demo/bench=init/Description=Create%20MAM%20project](https://mol.hyoo.ru/#!demo=mol\_button\_demo/bench=init/Description=Create%20MAM%20project)

```
git clone https://github.com/hyoo-ru/mam.git ./mam && cd mam
npm install && npm start
```

&#x20;

</details>

<details>

<summary>Какие плагины для IDE обязательны для $mol?</summary>

В $mol добавляется новый синтаксис .tree, поэтому для его подсветки обязательно нужен плагин [https://github.com/nin-jin/tree.d#ide-support](https://github.com/nin-jin/tree.d#ide-support) .\
\
Также в $mol строго определёны холиварные темы - табы или конфиги. \
[https://github.com/hyoo-ru/mam/blob/master/.editorconfig](https://github.com/hyoo-ru/mam/blob/master/.editorconfig) . Это нужно, чтобы рабочее окружение у всего проекта было строго определено 1 раз для всех. \
Для этого потребуется плагин Editor Config, который настраивает IDE по этому конфигу.\
\
Полный перечень плагинов тут: [https://mol.hyoo.ru/#!Description=Setup%20your%20editor](https://mol.hyoo.ru/#!Description=Setup%20your%20editor)

</details>
