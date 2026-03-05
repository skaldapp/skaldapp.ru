---
title: HTML
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Встраивание [HTML](https://ru.wikipedia.org/wiki/HTML){target="_blank"}

Одна из мощных возможностей Markdown — способность напрямую встраивать HTML-код, что обеспечивает более богатую выразительность и функциональные расширения для ваших документов.

### Строчные HTML-элементы

Вы можете использовать HTML-теги напрямую в Markdown:

```Markdown

Это абзац с <strong>жирным текстом</strong> и <em>курсивом</em>.

Вы можете использовать <code>строчный код</code> или <mark>выделенный текст</mark>.

Вот <a href="https://skaldapp.github.io/skaldapp/" target="_blank">внешняя ссылка</a>.

```

::elCard

Это абзац с <strong>жирным текстом</strong> и <em>курсивом</em>.

Вы можете использовать <code>строчный код</code> или <mark>выделенный текст</mark>.

Вот <a href="https://skaldapp.github.io/skaldapp/" target="_blank">внешняя ссылка</a>.

::

### Блочные HTML-элементы

```HTML

<div>
  <h4>Информация</h4>
  <p>Это информационное окно, созданное с помощью HTML.</p>
</div>

<blockquote style="border-left: 4px solid #007bff; padding-left: 1rem; color: #657d;">
  <p>Это цитата с пользовательским стилем.</p>
  <footer>—— Источник</footer>
</blockquote>

```

::elCard

<div>
  <h4>Информация</h4>
  <p>Это информационное окно, созданное с помощью HTML.</p>
</div>

<blockquote style="border-left: 4px solid #007bff; padding-left: 1rem; color: #657d;">
  <p>Это цитата с пользовательским стилем.</p>
  <footer>—— Источник</footer>
</blockquote>

::

### Смешанные HTML-элементы

```Markdown

<div style="text-align: center;">

#### Центрированный заголовок
  
Это абзац внутри <strong>центрированного</strong> контейнера.

</div>

```

<elCard>

<div style="text-align: center;">

#### Центрированный заголовок

Это абзац внутри <strong>центрированного</strong> контейнера.

</div>

</elCard>
