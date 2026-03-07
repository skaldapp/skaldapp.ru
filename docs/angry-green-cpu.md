---
title: Профессионально
icon: twemoji:page-facing-up
attrs:
  un-cloak: true
template: true
---

# Skald это профессионально

## Использование Vue в Markdown

В Skald каждый Markdown-файл компилируется в HTML, а затем обрабатывается как однофайловый компонент Vue. Это означает, что вы можете использовать любые возможности Vue внутри Markdown, включая динамический шаблонизатор, использование компонентов Vue или произвольную логику компонентов Vue на странице, добавив тег `<script>`.

<elMenu mode="horizontal" :router="true" :default-active="$route.path"><elMenuItem v-for="{ name, to, frontmatter: { title } } in doc.$children" :index="to" class="!px-5">{{ title ?? name }}</elMenuItem></elMenu>

:RouterView

<script setup>
import { inject } from "vue";

const docs = inject("docs");
const doc = docs[$id];
</script>
