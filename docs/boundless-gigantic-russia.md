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

const fibonacci=n=>~-n<=0?n:fibonacci(--n)+fibonacci(--n);

console.log(fibonacci(10)); // 55

```

````

Выведет следующий результат:

```JavaScript

const fibonacci=n=>~-n<=0?n:fibonacci(--n)+fibonacci(--n);

console.log(fibonacci(10)); // 55

```

## Таблицы

```Markdown

| Выравнивание слева | Выравнивание по центру | Выравнивание справа |
| :----------------- | :--------------------: | ------------------: |
| Контент 1          |        Контент 1       |           Контент 1 |
| Контент 2          |        Контент 2       |           Контент 2 |
| Контент 3          |        Контент 3       |           Контент 3 |

```

::elCard

| Выравнивание слева | Выравнивание по центру | Выравнивание справа |
| :----------------- | :--------------------: | ------------------: |
| Контент 1          |        Контент 1       |           Контент 1 |
| Контент 2          |        Контент 2       |           Контент 2 |
| Контент 3          |        Контент 3       |           Контент 3 |

::

## Математические формулы

Используйте двойные знаки доллара $$ для заключения формул, которые будут отображаться на отдельной центрированной строке. Для примера уравнение Шрёдингера:

```

$$
i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \hat{H}\Psi(\mathbf{r},t)
$$

```

::elCard

$$
i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \hat{H}\Psi(\mathbf{r},t)
$$

::

## Изображения

```Markdown

![Markdown](uploads/markdown.png) 🤗 ![](uploads/markdown.png "Markdown Logo") 🤗 ![Markdown](uploads/markdown.png "Markdown Logo")

![1.00](uploads/elder.jpg "Старец")

```

![Markdown](uploads/markdown.png)[🤗]{.text-5xl.mx-4}![](uploads/markdown.png "Markdown Logo")[🤗]{.text-5xl.mx-4}![Markdown](uploads/markdown.png "Markdown Logo")

![1.00](uploads/elder.jpg "Старец")

