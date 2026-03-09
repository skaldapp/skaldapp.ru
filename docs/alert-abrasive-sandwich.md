---
title: Markdown Components
description: Добавляйте собственные компоненты прямо в Markdown — поддерживаются как блочный, так и строчный синтаксис, пропсы, слоты и вложенные элементы.
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Компоненты

Добавляйте собственные компоненты прямо в Markdown — поддерживаются как блочный, так и строчный синтаксис, пропсы, слоты и вложенные элементы.

Skald добавляет в Markdown поддержку компонентов — теперь вы можете вставлять собственные UI-элементы прямо в текст, не жертвуя его читаемостью.

### Блочные компоненты

Для блочных компонентов применяется синтаксис `::имя-компонента`, и они всегда размещаются на отдельной строке.

```Markdown

::component-name{prop1="value1" prop2="value2"}
Content inside the component

Can have **markdown** and other elements
::

```

#### Примеры

```Markdown
::alert{type="info"}
This is an important message!
::

::card{title="My Card"}
Card content with **markdown** support
::

::divider
::
```

### Инлайн-компоненты

Инлайн-компоненты используют синтаксис `:имя-компонента` и могут размещаться непосредственно в тексте:

```Markdown
Check out this :icon-star component in the middle of text.

Click the :button[Submit]{type="primary"} to continue.

The status is :badge[Active]{color="green"} right now.
```

<br />

| Синтаксис                     | Описание                                |
| :---------------------------- | :-------------------------------------- |
| `:icon-check`                 | Простой инлайн-компонент                |
| `:badge[New]`                 | Инлайн-компонент с контентом            |
| `:badge[New]{color="blue"}`   | Инлайн-компонент с контентом и пропсами |
| `:tooltip{text="Hover text"}` | Инлайн-компонент только с пропсами      |

### Свойства компонентов

Используйте синтаксис `{...}` для простых свойств:

```Markdown
::component{prop="value"}
<!-- Standard key-value pair -->
::

::component{bool}
<!-- Boolean property (becomes :bool="true" in AST) -->
::

::component{#custom-id}
<!-- ID attribute -->
::

::component{.class-name}
<!-- CSS class -->
::

::component{.class-one .class-two}
<!-- Multiple CSS classes -->
::

::component{obj='{"key": "value"}'}
<!-- Object/JSON value -->
::

::component{multiple="props" bool #id .class}
<!-- Multiple properties combined -->
::
```

### Слоты компонентов

Блочные компоненты поддерживают именованные слоты с использованием синтаксиса `#slot-name`:


```Markdown
::card
#header
# Card Title

#content
This is the main content of the card

#footer
Footer text here
::
```

## Вложенные компоненты

Компоненты могут быть вложены друг в друга с использованием дополнительных двоеточий:

```Markdown
::outer-component
Content in outer

:::inner-component{variant="compact"}
Content in inner
:::

More content in outer
::
```
