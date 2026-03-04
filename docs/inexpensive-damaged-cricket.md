---
title: Skald
description: Skald - это современный инструмент для работы с текстом и веб-разработки.
attrs:
  un-cloak: true
  class:
    - max-w-none
    - prose
    - prose-slate
    - prose-sm
    - sm:prose-base
    - dark:prose-invert
    - min-h-dvh
template: true
icon: twemoji:page-facing-up
script:
  - type: importmap
    innerHTML: |
      {
        "imports": {
          "@vueuse/core": "https://cdn.jsdelivr.net/npm/@vueuse/core/dist/index.js",
          "@vueuse/shared": "https://cdn.jsdelivr.net/npm/@vueuse/shared/dist/index.js",
          "element-plus": "https://cdn.jsdelivr.net/npm/element-plus@2/dist/index.full.min.mjs"
        }
      }
---

<ul id="menu" class="not-prose" container mx-auto px-4 flex flex-wrap gap-3 w-full text-sm border-b-2 py-4 mt-2 mb-24 font-medium>
<li><RouterLink to="/" id="logo">SK<i i-fa7-solid-mountain align-text-bottom size-5 />LD</RouterLink></li>
<li v-for="{ frontmatter: { title }, to, id } in the.$children.slice(1)" :key="id"><RouterLink :to>{{ title }}</RouterLink></li>
<li><a href="https://github.com/skaldapp" target="_blank" rel="noopener noreferrer"><i i-carbon-logo-github align-middle size-6 /></a></li>
<li><i i-carbon-sun dark-i-carbon-moon align-middle size-6 dark-size-6 cursor-pointer @click="toggleDark()" /></li>
</ul>

::div{.min-h-dvh.container.mx-auto.px-4}

:RouterView

::

::div{.bg-[var(--nord6)].dark-bg-[var(--nord0)].mt-32}

:::div{.container.mx-auto.px-4.py-8}

:h3[🚀 Готовы попробовать Skald?]

Начните творить, создавать и развивать свои проекты **уже сегодня**! Skald – это ваш **надежный спутник** в мире текстов и веб-разработки.

:::

::

:elBacktop

<script setup lang="ts">
import { getCurrentInstance, inject } from "vue";
import ElementPlus from "element-plus";
import { useDark, useToggle } from "@vueuse/core";

const toggleDark = useToggle(useDark());
const docs = inject("docs");
const the = docs[$id];

window.__vue_app__.use(ElementPlus);

</script>

<style>
@import url("https://cdn.jsdelivr.net/npm/element-plus@2/theme-chalk/index.css");
@import url("https://cdn.jsdelivr.net/npm/element-plus@2/theme-chalk/dark/css-vars.css");

:root {
  --nord0: #2E3440;
  --nord1: #3B4252;
  --nord2: #434C5E;
  --nord3: #4C566A;
  --nord4: #D8DEE9;
  --nord5: #E5E9F0;
  --nord6: #ECEFF4;
  --nord7: #8FBCBB;
  --nord8: #88C0D0;
  --nord9: #81A1C1;
  --nord10: #5E81AC;
  --nord11: #BF616A;
  --nord12: #D08770;
  --nord13: #EBCB8B;
  --nord14: #A3BE8C;
  --nord15: #B48EAD;
}
</style>

<style lang="postcss">
body {
  @apply dark-bg-[var(--nord1)];
}

html:not(.dark) #dark,
html.dark #light {
  display: none !important;
}

</style>

<style scoped lang="postcss">
#menu {
  @apply border-[var(--nord8)];

  & li:nth-last-child(2) {
    @apply ml-auto -mr-4;
  }

  & a.router-link-active:not(#logo) {
    @apply bg-[var(--nord8)] text-[var(--nord6)];
  }
}

#menu a {
  @apply "text-[var(--nord0)] transition px-3 py-2 rounded-md hover-text-[var(--nord10)] dark-text-[var(--nord6)]";
}
</style>
