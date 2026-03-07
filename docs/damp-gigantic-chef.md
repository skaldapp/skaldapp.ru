---
title: HTML
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Строчные HTML-элементы

Вы можете использовать HTML-теги напрямую в Markdown:

**Разметка**

```Markdown

Это абзац с <strong>жирным текстом</strong> и <em>курсивом</em>.

Вы можете использовать <code>строчный код</code> или <mark>выделенный текст</mark>.

Вот <a href="https://skaldapp.github.io/skaldapp/" target="_blank">внешняя ссылка</a>.

```

::elCard{header="Результат" header-class="font-bold"}

Это абзац с <strong>жирным текстом</strong> и <em>курсивом</em>.

Вы можете использовать <code>строчный код</code> или <mark>выделенный текст</mark>.

Вот <a href="https://skaldapp.github.io/skaldapp/" target="_blank">внешняя ссылка</a>.

::

## Блочные HTML-элементы

**Разметка**

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

::elCard{header="Результат" header-class="font-bold"}

<div>
  <h4>Информация</h4>
  <p>Это информационное окно, созданное с помощью HTML.</p>
</div>

<blockquote style="border-left: 4px solid #007bff; padding-left: 1rem; color: #657d;">
  <p>Это цитата с пользовательским стилем.</p>
  <footer>—— Источник</footer>
</blockquote>

::

## Смешанные HTML-элементы

**Разметка**

```Markdown

<div style="text-align: center;">

#### Центрированный заголовок
  
Это абзац внутри <strong>центрированного</strong> контейнера.

</div>

```

<elCard header="Результат" header-class="font-bold">

<div style="text-align: center;">

#### Центрированный заголовок

Это абзац внутри <strong>центрированного</strong> контейнера.

</div>

</elCard>
