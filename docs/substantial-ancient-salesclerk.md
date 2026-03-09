---
title: Attributes
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Аттрибуты

Добавьте пользовательские классы, идентификаторы (ID), стили и атрибуты данных к стандартным элементам Markdown с помощью синтаксиса фигурных скобок.

Skald позволяет добавлять пользовательские атрибуты к стандартным элементам Markdown, используя синтаксис `{...}` сразу после элемента.

### Аттрибуты элементов

#### Strong/Bold

```Markdown

**bold text**{.highlight #important}
**bold text**{data-value="custom"}
**bold text**{bool}

```

#### Italic/Emphasis

```Markdown

*italic text*{.emphasized}
*italic text*{#custom-id}

```

#### Links

```Markdown

[Link text](url){target="_blank" rel="noopener"}
[Link text](url){.button .primary}
[External](https://example.com){target="_blank" .external-link}

```

#### Images

```Markdown

![Alt text](image.png){.responsive width="800" height="600"}
![Logo](logo.svg){.logo #site-logo}

```

#### Inline Code

```Markdown

`code snippet`{.language-js}
`variable`{data-type="string"}

```

### Типы аттрибутов

| Синтаксис                  | Вывод                 | Описание                   |
| :------------------------- | :-------------------- | :------------------------- |
| `{bool}`                   | `:bool="true"`        | Булевый атрибут            |
| `{#my-id}`                 | `id="my-id"`          | Атрибут идентификатора     |
| `{.my-class}`              | `class="my-class"`    | Атрибут класса             |
| `{key="value"}`            | `key="value"`         | Атрибут типа ключ-значение |
| `{:data='{"key": "val"}'}` | `data={"key": "val"}` | Атрибут JSON объекта       |

### Span атрибуты

Добавьте к любому фрагменту текста пользовательские атрибуты, обернув его в `<span>`. Так можно стилизовать отдельные части текста или добавлять метаданные без необходимости создавать собственные компоненты.

### Синтаксис

```Markdown
[text content]{attributes}
```

Текст указывается в квадратных скобках `[...]`, а после них в фигурных скобках `{...}` задаются атрибуты.

### Примеры

#### Class:

```Markdown
This is [highlighted text]{.highlight} in a paragraph.
```

```html
<p>This is <span class="highlight">highlighted text</span> in a paragraph.</p>
```

#### Multiple classes:

```Markdown
[Important]{.badge .primary} information here.
```

```html
<p><span class="badge primary">Important</span> information here.</p>
```

#### ID:

```Markdown
Reference this [specific text]{#ref-1} later.
```

```html
<p>Reference this <span id="ref-1">specific text</span> later.</p>
```

#### Inline styles:

```Markdown
[Blue text]{style="color: blue; font-weight: bold"}
```

```html
<p><span style="color: blue; font-weight: bold">Blue text</span></p>
```

#### Data attributes:

```Markdown
[Earth]{data-planet="earth" data-type="terrestrial"}
```

```html
<p><span data-planet="earth" data-type="terrestrial">Earth</span></p>
```

#### Combined attributes:

```Markdown
[Status: Active]{#status .badge .success data-state="active"}
```

```html
<p><span id="status" class="badge success" data-state="active">Status: Active</span></p>
```

### Вложенный Markdown

Внутри span-элементов можно использовать вложенное форматирование Markdown.

```Markdown
[**Bold** and *italic* text]{.highlight}
```

```html
<p><span class="highlight"><strong>Bold</strong> and <em>italic</em> text</span></p>
```
