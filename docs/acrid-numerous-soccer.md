---
title: Эффективно
icon: twemoji:page-facing-up
attrs:
  un-cloak: true
template: true
---

# Skald это эффективно

[HTML](https://developer.mozilla.org/ru/docs/Web/HTML){target="_blank"} (от англ. HyperText Markup Language — «язык гипертекстовой разметки») — стандартизированный язык гипертекстовой разметки документов для просмотра веб-страниц в браузере. Язык гипертекстовой разметки HTML был разработан британским учёным Тимом Бернерсом-Ли как язык для обмена научной и технической документацией, пригодный для использования людьми, не являющимися специалистами в области вёрстки.

Одна из мощных возможностей Skald — способность напрямую встраивать HTML-код, что обеспечивает более богатую выразительность и функциональные расширения для ваших документов.

<elMenu mode="horizontal" :router="true" :default-active="$route.path"><elMenuItem v-for="{ name, to, frontmatter: { title } } in doc.$children" :index="to" class="!px-5">{{ title ?? name }}</elMenuItem></elMenu>

:RouterView

<script setup>
import { inject } from "vue";

const docs = inject("docs");
const doc = docs[$id];
</script>