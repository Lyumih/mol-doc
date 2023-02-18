---
description: Инструкция по локализации проекта в $mol
---

# Лакализация

Процесс локализации проекта может проходить двумя разными подходами: через файлы ресурсов проекта и через запрос к веб серверу онлайн. В $mol по умолчанию используется 1 подход.&#x20;

Локализация в $mol настроина по умолчанию из коробки. Небольшое введение по локализации есть в этой [статье](https://page.hyoo.ru/#!=jfketb\_3qo2ad/View%22jfketb\_3qo2ad%22.Details=%D0%9B%D0%BE%D0%BA%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%B2%D0%BE%20view.tree) .

<img src="../.gitbook/assets/image (4).png" alt="" data-size="original">![](<../.gitbook/assets/image (2).png>)![](../.gitbook/assets/image.png)![](<../.gitbook/assets/image (5).png>)

Рассмотрим локализацию на примере приложения Quine [https://mol.js.org/app/quine/-/](https://mol.js.org/app/quine/-/) , его исходники лежат здесь: [https://github.com/hyoo-ru/mam\_mol/tree/master/app/quine](https://github.com/hyoo-ru/mam\_mol/tree/master/app/quine)



Процесс локализации состоит из нескольких шагов:

1. Постав знак _**@**_ перед значением свойства компонента, которое нужно будет перевести на разные языки. Ключ для перевода будет автоматически сгенерирован из файла [https://github.com/hyoo-ru/mam\_mol/blob/master/app/quine/quine.view.tree#L2](https://github.com/hyoo-ru/mam\_mol/blob/master/app/quine/quine.view.tree#L2) и его можно будет посмотреть локально в папке /mam/mol/app/quine/-view.tree/quine.view.tree.locale=en.json после запуска проекта.

```
// title - свойство заголовка
// @ - значение для данного свойства будет автоматически переведено
// \Quine - Строка для перевода по умолчанию для en локали, её переводить на en не нужно будет.
    title @ \Quine - Application that prints self sources

```

2. Создать в папке компонента файл с переводами под каждую локаль. Файл будет называться также, как и compnonent с приставкой compnent**.locale=ru.json ,** где ru -  выбранная локаль. вот ссылка на файл: [https://github.com/hyoo-ru/mam\_mol/blob/master/app/quine/quine.locale%3Dru.json](https://github.com/hyoo-ru/mam\_mol/blob/master/app/quine/quine.locale%3Dru.json) . EN локаль достаётся автоматически из компонента. "$mol\_app\_quine\_title" - это ключ, полученный согласно **fqn нотации** - расположение компонента в проекте + имя свойства или компонента.

```
{
	"$mol_app_quine_title": "Quine - приложение, выводящее собственные исходные коды"
}
```

На этом основные шаги по переводу закончены. Дальше нужно обедиться, что в браузере локализация правильно отрабатывает.&#x20;

1. Открываем браузер с проектом, например, [https://mol.js.org/app/quine/-/](https://mol.js.org/app/quine/-/) и открываем консоль разработчика.
2. В консоли вводим команду для смены локали на проекте `$mol_locale.lang('en')` или `$mol_locale.lang('ru')`. Эта команда поменяет заголовок и подсказку для кнопки копирования на сайте. Если ввести локаль, которой нет `$mol_locale.lang('it')` - то будет примерена локаль по умолчанию ('en'). Ознакомьтесь с неольшим исходником по локализации [https://github.com/hyoo-ru/mam\_mol/blob/master/locale/locale.ts](https://github.com/hyoo-ru/mam\_mol/blob/master/locale/locale.ts)  .<img src="../.gitbook/assets/image (4).png" alt="" data-size="original">![](<../.gitbook/assets/image (2).png>)
3. Локаль хронится в localStorage сайта, поэтому при перезапуске браузера у пользователя сохранится выбранный им язык. <img src="../.gitbook/assets/image (6).png" alt="" data-size="original">
4. Если нужно получить переводы для всех ключей на сайте по выбранной локали, то нужно выполнить команду `$mol_locale.texts('ru')` и получите все ключи. Даже те, которые используются в других компонентах. Их можно будет отследить по названию ключа, т.к. оно указывает на путь до компонента + свойство. Исходник команды лежит тут: [https://github.com/hyoo-ru/mam\_mol/blob/master/locale/locale.ts#L39-L50](https://github.com/hyoo-ru/mam\_mol/blob/master/locale/locale.ts#L39-L50)

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>



Это пример позволяет начать делать быструю и удобную локализацию на проекте. \
Со временем, когда проект будет разрастаться и потребуется профессиональные переводы, лучше будет перейти на 1 из платных сервисов, которые будут подгружать выбранную локаль из облако прямо на сайт. Например, [https://poeditor.com/](https://poeditor.com/) или [https://locize.com/](https://locize.com/) .&#x20;
