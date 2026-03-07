---
title: Расширения
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Код

Используйте три обратные кавычки `` ` `` для обрамления кода, укажите название языка после открывающих `` ` `` для включения подсветки синтаксиса:

````Markdown

```JavaScript

const fibonacci = (length) => Array.from({ length }, function (_, $) { return this[$] = this[$ - 1] + this[$ - 2] || $ }, []);

console.log(fibonacci(10)); // [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

```

````

Выведет следующий результат:

```JavaScript

const fibonacci = (length) => Array.from({ length }, function (_, $) { return this[$] = this[$ - 1] + this[$ - 2] || $ }, []);

console.log(fibonacci(10)); // [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

```

## Таблицы

**Разметка**

```Markdown

| Выравнивание слева | Выравнивание по центру | Выравнивание справа |
| :----------------- | :--------------------: | ------------------: |
| Контент 1          |        Контент 1       |           Контент 1 |
| Контент 2          |        Контент 2       |           Контент 2 |
| Контент 3          |        Контент 3       |           Контент 3 |

```

::elCard{header="Результат" header-class="font-bold"}

| Выравнивание слева | Выравнивание по центру | Выравнивание справа |
| :----------------- | :--------------------: | ------------------: |
| Контент 1          |        Контент 1       |           Контент 1 |
| Контент 2          |        Контент 2       |           Контент 2 |
| Контент 3          |        Контент 3       |           Контент 3 |

::

## Математические формулы

Используйте двойные знаки доллара $$ для заключения формул, которые будут отображаться на отдельной центрированной строке. Для примера уравнение Шрёдингера:

**Разметка**

```

$$
i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \hat{H}\Psi(\mathbf{r},t)
$$

```

::elCard{header="Результат" header-class="font-bold"}

$$
i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \hat{H}\Psi(\mathbf{r},t)
$$

::

## Изображения

**Разметка**

```Markdown

![Markdown](uploads/markdown.png) - ![](uploads/markdown.png "Markdown Logo") - ![Markdown](uploads/markdown.png "Markdown Logo")

![1.00](uploads/elder.jpg "Старец")

```

::elCard{header="Результат" header-class="font-bold"}

![Markdown](uploads/markdown.png) - ![](uploads/markdown.png "Markdown Logo") - ![Markdown](uploads/markdown.png "Markdown Logo")

![1.00](uploads/elder.jpg "Старец")

::