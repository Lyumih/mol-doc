---
description: Все вопросы, которые относятся к git и $mol
---

# Как работать в $mol с git?

<details>

<summary>Что нужно клонировать из git, чтобы начать разработку?</summary>

Нужно клонировать рабочее окружение и уже в нём начать работать.

```
git clone https://github.com/hyoo-ru/mam.git ./mam && cd mam
npm install && npm start
```

Подробнее тут: [https://mol.hyoo.ru/#!demo=mol\_button\_demo/bench=init/Description=Create%20MAM%20project](https://mol.hyoo.ru/#!demo=mol\_button\_demo/bench=init/Description=Create%20MAM%20project)

</details>

<details>

<summary>Что такое монорепотозиторий и полирепозиторий?</summary>

Подробнее вы можете узнать [здесь](https://mol.hyoo.ru/#!section=articles/author=hyoo-ru/repo=HabHub/article=4/Articles.Datails\_text=%D0%9C%D0%BE%D0%BD%D0%BE%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8%20%D0%B8%20%D0%BF%D0%BE%D0%BB%D0%B8%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8) .\
МАМ поддерживает работу с этими 2 типами репозиториев и предоставляет свои команды npm для работы с ними.

Также можно для лучшего понимания видов репозиториев можно посмотреть данный сайт [https://monorepo.tools/](https://monorepo.tools/)

</details>

<details>

<summary>Как установить какой-либо модуль, проект?</summary>

Для установки какого-либо модуля в mam достаточно команды

```
yarn start hyoo/app
```

Эта команда установит данную версию модуля в деррикторию mam и все зависимости к нему. [https://github.com/hyoo-ru/apps.hyoo.ru](https://github.com/hyoo-ru/apps.hyoo.ru)\
\
Подробнее можете прочитать [здесь](https://mol.hyoo.ru/#!section=articles/author=hyoo-ru/repo=HabHub/article=4/Articles.Datails\_text=%D0%9C%D0%BE%D0%BD%D0%BE%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8%20%D0%B8%20%D0%BF%D0%BE%D0%BB%D0%B8%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8)\


</details>

<details>

<summary>Как выложить свой модуль на GitHub Pages / npm?</summary>

Инструкция по публикации модулей в интернете уже написана. Она начинается с разела ["Монорепозитории и полирепозитории" ](https://mol.hyoo.ru/#!section=articles/author=hyoo-ru/repo=HabHub/article=4/Articles.Datails\_text=%D0%9C%D0%BE%D0%BD%D0%BE%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8%20%D0%B8%20%D0%BF%D0%BE%D0%BB%D0%B8%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8)из статьи [Введение в $mol. Часть 1. Модульная система МАМ.](https://mol.hyoo.ru/#!section=articles/author=hyoo-ru/repo=HabHub/article=4)\
\
Необходимо обратить внимание на несколько моментов

* Пример готового модуля на GitHub: [https://github.com/hyoo-ru/apps.hyoo.ru](https://github.com/hyoo-ru/apps.hyoo.ru)&#x20;
* Чтобы использовать начать модуль, достаточно команды `yarn start hyoo/app`&#x20;
* Модуль будет установлен в деррикторию проекта mam согласно его имени
* Если до этого не было опыта работа с полирепозиторием, осознать, что  git репозитории могут быть вложены друг в друга как матрёшка и работать изолированно достаточно сложно.
* Если у вас остались вопросы по публикации, задайти их нам в чат в телеграмме: [https://t.me/mam\_mol](https://t.me/mam\_mol). Сообщество поможет разобраться и настроить публикацию пакетов



</details>

<details>

<summary>Как работать с  Fork-ом модуля?</summary>

Fork - это копия репозитория, через который вы можете независимо вносить изменения в своём репозитории и потом создавать Pull Requests для внесения этих изменений в основной репозиторий модуля.\
Вы можете ознакомиться с данной темой здесь: [https://www.atlassian.com/ru/git/tutorials/syncing](https://www.atlassian.com/ru/git/tutorials/syncing)

Или здесь : [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks) . Прочтите все разделы Working with fork - это ответит на большинство вопрос связанных с работой fork\


</details>
