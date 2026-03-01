---
title: Просто
description: Easy to use
icon: twemoji:page-facing-up
template: true
attrs:
  un-cloak: true
---

# Skald это просто

Markdown — это **лёгкий язык разметки**, который позволяет форматировать текст с помощью простых и интуитивно понятных синтаксических конструкций. Он был создан в **2004 году Джоном Грубером** (John Gruber) и Аароном Шварцем (Aaron Swartz) с целью сделать текст максимально читаемым как в исходном виде, так и после преобразования в HTML или другие форматы.

Skald поддерживает создание текстов формате Markdown, как в визуальном, так и в текстовом режиме, что позволяет легко и быстро оформлять контент с помощью простых и понятных синтаксических конструкций.

<elMenu mode="horizontal" :router="true" :default-active="$route.path"><elMenuItem v-for="{ name, to, frontmatter: {title} } in doc.$children" :index="to" class="!px-5">{{ title ?? name }}</elMenuItem></elMenu>

:RouterView

<script setup>
import { inject } from "vue";

const docs = inject("docs");
const doc = docs[$id];
</script>
