---
title: Стили CSS
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Стилизация Markdown с помощью CSS

Markdown предоставляет лаконичный синтаксис для форматирования текста, но CSS-стили могут сделать ваши документы более красивыми и профессиональными.

:elAlert{.not-prose title="scoped" type="warning" description="Стили применяются только к текущей странице, если использован аттрибут scoped." show-icon :closable="false"}

**Разметка**

```html

<style scoped>
.highlight {
  background-color: #fff3cd;
  color: black;
  padding: 10px;
  border-left: 4px solid #ffc107;
}
</style>

<div class="highlight">
Это важный выделенный параграф.
</div>

```

::elCard{header="Результат" header-class="font-bold"}


<style scoped>
.highlight {
  background-color: #fff3cd;
  color: black;
  padding: 10px;
  border-left: 4px solid #ffc107;
}
</style>

<div class="highlight">
Это важный выделенный параграф.
</div>

::

Для тех же целей можно использовать классы из Tailwind CSS.

**Разметка**

```html

<style lang="postcss" scoped>
.highlight-tw {
  @apply bg-amber-100 text-black p-3 border-l-4 border-yellow-400;
}
</style>

<div class="highlight-tw">
Это важный выделенный параграф с использованием классов Tailwind CSS.
</div>

```

::elCard{header="Результат" header-class="font-bold"}

<style lang="postcss" scoped>
.highlight-tw {
  @apply bg-amber-100 text-black p-3 border-l-4 border-yellow-400;
}
</style>

<div class="highlight-tw">
Это важный выделенный параграф с использованием классов Tailwind CSS.
</div>

::

Стили также можно подключить из внешних файлов, например, из CDN:

**Разметка**

```html

<style scoped src="https://cdn.jsdelivr.net/npm/hover.css/css/hover-min.css"></style>

<div class="hvr-buzz">Наведи на меня курсор!!!</div>

```

::elCard{header="Результат" header-class="font-bold"}

<style scoped src="https://cdn.jsdelivr.net/npm/hover.css/css/hover-min.css"></style>

<div class="hvr-buzz">Наведи на меня курсор!!!</div>

::