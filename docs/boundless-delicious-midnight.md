---
title: Семантика
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Семантический объект страницы

Каждая страница содержит статическую константу `$id` с персональным идентификационным номером, который всегда совпадает с названием файла в директории `docs`.

Так же есть возможность инжектировать ассоциативный массив всех семантических объектов страниц и получить идентификационный номер выбранной в данный момент страницы из объекта роутера.

```JavaScript

/** Импортируем вычислитель и инжектор */
import { computed, inject } from "vue";
/** Импортируем композабл выбранного роута */
import { useRoute } from "vue-router";
/** Получаем объект выбранного роута */
const route = useRoute();
/** Инжектируем массив семантических объектов страниц сайта */
const docs = inject("docs");
/** Получаем семантический объект данной станицы */
const doc = docs[$id];
/** Вычисляем семантический объект выбранной страницы */
const current = computed(() => docs[route.name]);

```

## Пример использования

**Разметка**

::div{v-pre}

```HTML

<h3>{{ doc.parent.title }}</h3>
<ul>
    <li v-for="{title} in doc.$siblings">{{ title }}</li>
</ul>

```

::

::elCard{header="Результат" header-class="font-bold"}

<h3>{{ doc.parent.frontmatter.title }}</h3>
<ul>
    <li v-for="{ frontmatter: { title } } in doc.$siblings">{{ title }}</li>
</ul>

::

## Список аттрибутов

* **id** - Уникальный идентификатор страницы doc

* **name** - Короткое имя страницы doc, используется для формирования атрибута path

* **frontmatter** - Объект frontmatter страницы doc

* **parent** - Родительская страница doc

* **next** - Следующая страница от doc в массиве siblings

* **prev** - Предыдущая страница от doc в массиве siblings

* **index** - Индекс страницы doc в массиве siblings

* **children** - Дочерние страницы doc

* **siblings** - Массив одноуровневых страниц со страницей doc

* **path** - Относительный путь до страницы doc

* **branch** - Массив страниц от корневой до страницы doc

* **to** - Урл страницы для подстановки в `<RouterLink>`

Дополнительно существуют аттрибуты, которые начинаются с символа `$` ($children, $index, $siblings, $next, $prev, $branch, $parent) и содержат соответстующие страницы, отфильтрованные по параметру hidden в frontmatter.

<script setup>
import { inject } from "vue";
const docs = inject("docs");
const doc = docs[$id];
</script>
