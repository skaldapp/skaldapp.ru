---
title: Tailwind CSS
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## [Tailwind CSS](https://tailwindcss.ru/){target="_blank"} уже интегрирован и готов к использованию

В редакторе Skald классы Tailwind CSS доступны сразу, без каких-либо дополнительных действий: не нужно подключать библиотеку, настраивать сборку или редактировать конфигурацию. Просто пишите HTML и применяйте готовые Tailwind-классы — всё работает по умолчанию.

:elAlert{.not-prose title="FOUC" type="warning" description="Для пердотвращения дребезга контента при загрузке, используйте атрибут `un-cloak` в корневом элементе страницы." show-icon :closable="false"}

**Разметка**

```HTML

<button class="m-2 bg-blue-400 hover:bg-blue-500 text-sm text-white font-mono font-light py-2 px-4 rounded border border-blue-200 dark:bg-blue-500 dark:hover:bg-blue-600">
  Button
</button>

```

::elCard{.not-prose header="Результат" header-class="font-bold"}

<button class="m-2 bg-blue-400 hover:bg-blue-500 text-sm text-white font-mono font-light py-2 px-4 rounded border border-blue-200 dark:bg-blue-500 dark:hover:bg-blue-600">
  Button
</button>

::

Или даже так:

**Разметка**

```HTML

<button m-2 bg="blue-400 hover:blue-500 dark:blue-500 dark:hover:blue-600" text="sm white" font="mono light" p="y-2 x-4" border="~ rounded blue-200">
  Button
</button>

```

::elCard{.not-prose header="Результат" header-class="font-bold"}

<button m-2 bg="blue-400 hover:blue-500 dark:blue-500 dark:hover:blue-600" text="sm white" font="mono light" p="y-2 x-4" border="~ rounded blue-200">
  Button
</button>

::

Допускается также использовать сокращенную запись для компонентов, к примеру `text-red` вместо `class="text-red"`:

**Разметка**

```html

<!-- обычная запись -->

<span class="text-red">red text</span>
<div class="flex">flexbox</div>
I'm feeling <span class="i-line-md-emoji-grin"></span> today!

<!-- сокращенная запись -->

<text-red>red text</text-red>
<flex>flexbox</flex>
I'm feeling <i-line-md-emoji-grin /> today!

```

::elCard{.not-prose header="Результат" header-class="font-bold"}

<text-red>red text</text-red>
<flex>flexbox</flex>
I'm feeling <i-line-md-emoji-grin /> today!

::

## Иконки

Любая иконка из проекта Iconify доступна по первому требованию. Просто добавьте класс `i-<имя_коллекции>:<имя_иконки>` к любому элементу, и иконка появится. Например, `i-carbon:sun` отобразит иконку солнца из коллекции Carbon.

**Разметка**

```html

<div class="flex items-center gap-x-4 text-4xl p-2 mt-4">
    <div class="i-ph:anchor-simple-thin"></div>
    <div class="i-mdi:alarm text-orange-400 hover:text-teal-400"></div>
    <div class="w-2em h-2em i-logos:vue transform transition-800 hover:rotate-180"></div>
    <div class="i-carbon:sun dark:i-carbon:moon !w-2em !h-2em"></div>
    <div class="i-twemoji:grinning-face-with-smiling-eyes hover:i-twemoji:face-with-tears-of-joy"></div>
    <div class="text-base my-auto flex"><div class="i-carbon:arrow-left my-auto mr-1"></div> Hover it</div>
</div>

```

::elCard{.not-prose header="Результат" header-class="font-bold"}

<div class="flex items-center gap-x-4 text-4xl p-2 mt-4">
    <div class="i-ph:anchor-simple-thin"></div>
    <div class="i-mdi:alarm text-orange-400 hover:text-teal-400"></div>
    <div class="w-2em h-2em i-logos:vue transform transition-800 hover:rotate-180"></div>
    <div class="i-carbon:sun dark:i-carbon:moon !w-2em !h-2em"></div>
    <div class="i-twemoji:grinning-face-with-smiling-eyes hover:i-twemoji:face-with-tears-of-joy"></div>
    <div class="text-base my-auto flex"><div class="i-carbon:arrow-left my-auto mr-1"></div> Hover it</div>
</div>

::

## Типографика

:elAlert{.not-prose title="Проза" type="primary" description="Типографика включается путем добавления класса prose к элементу. Выключение можно сделать с помощью класса not-prose." show-icon :closable="false"}

**Разметка**

```html

<article class="prose prose-stone prose-xl dark:prose-invert">
  <h1>Чесночный хлеб с сыром: что говорит нам наука</h1>
  <p>
    В течение многих лет родители поддерживали пользу для здоровья от употребления в пищу чесночного хлеба с сыром
    для своих детей, и эта еда приобрела такой культовый статус в нашей культуре,
    что дети часто наряжаются теплым, сырным хлебом на Хэллоуин.
  </p>
  <p>
    Но недавнее исследование показывает, что знаменитая закуска может быть связана
    с серией случаев бешенства, возникающих по всей стране.
  </p>
</article>

```

::elCard{header="Результат" header-class="font-bold"}

<article class="prose-stone prose-xl dark:prose-invert">
  <h1>Чесночный хлеб с сыром: что говорит нам наука</h1>
  <p>
    В течение многих лет родители поддерживали пользу для здоровья от употребления в пищу чесночного хлеба с сыром
    для своих детей, и эта еда приобрела такой культовый статус в нашей культуре,
    что дети часто наряжаются теплым, сырным хлебом на Хэллоуин.
  </p>
  <p>
    Но недавнее исследование показывает, что знаменитая закуска может быть связана
    с серией случаев бешенства, возникающих по всей стране.
  </p>
</article>

::
