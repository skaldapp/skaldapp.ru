---
title: Эффективно
icon: twemoji:page-facing-up
attrs:
  un-cloak: true
template: true
---

# Skald это эффективно

<elMenu mode="horizontal" :router="true" :default-active="$route.path"><elMenuItem v-for="{ name, to, frontmatter: { title } } in doc.$children" :index="to" class="!px-5">{{ title ?? name }}</elMenuItem></elMenu>

:RouterView

<script setup>
import { inject } from "vue";

const docs = inject("docs");
const doc = docs[$id];
</script>