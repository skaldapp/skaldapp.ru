---
title: Форматирование
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Базовое форматирование

| **Эффект**    | **Синтаксис** | **Пример**          |
| ------------- | ------------- | ------------------- |
| Курсив        | `*текст*`     | *Курсив*            |
| Жирный        | `**текст**`   | **Жирный**          |
| Жирный курсив | `***текст***` | ***Жирный курсив*** |
| Зачеркивание  | `~~текст~~`   | ~~Зачеркивание~~    |

## Расширенное форматирование

| **Тип** | **Синтаксис** | **Пример**   |
| ------- | ------------- | ------------ |
| Код     | `const a=1;`  | `const a=1;` |
| Формула | `$E = mc^2$`  | $E = mc^2$   |

## Ссылки

**Разметка**

```Markdown

[Текст ссылки](https://skaldapp.ru)

[Ссылка с заголовком](https://skaldapp.ru "Заголовок ссылки")

```

::elCard{header="Результат" header-class="font-bold"}

[Текст ссылки](https://skaldapp.ru)

[Ссылка с заголовком](https://skaldapp.ru "Заголовок ссылки")

::

| **Тип**              | **Синтаксис**                                       | **Пример**                                        |
| -------------------- | --------------------------------------------------- | ------------------------------------------------- |
| Абсолютная ссылка    | `[skaldapp.ru](https://skaldapp.ru)`                | [skaldapp.ru](https://skaldapp.ru)                |
| Относительная ссылка | `[эффективно](/medium/)`                            | [эффективно](/medium/)                            |
| Ссылка на заголовок  | `[Базовое форматирование](#bazovoe-formatirovanie)` | [Базовое форматирование](#bazovoe-formatirovanie) |

:elAlert{.not-prose title="Оглавление" type="primary" description="Для формирования оглавления по всем заголовкам на странице используйте `[[toc]]`" show-icon :closable="false"}

## Автоссылки

**Разметка**

```Markdown

https://skaldapp.ru

skaldapp@outlook.com

```

::elCard{header="Результат" header-class="font-bold"}

<https://skaldapp.ru>

<skaldapp@outlook.com>

::

## Ссылка на изображение

**Разметка**

```Markdown

[![1.00](uploads/valkyrja.jpg)](https://skaldapp.ru)

```

::elCard{.not-prose header="Результат" header-class="font-bold"}

[![1.00](uploads/valkyrja.jpg)](https://skaldapp.ru)

::