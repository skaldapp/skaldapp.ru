---
title: Skald
description: Skald is a tool for creating and managing markdown content.
attrs:
  un-cloak: true
  class:
    - container
    - mx-auto
    - px-4
    - prose
    - prose-slate
    - prose-sm
    - sm:prose-base
    - dark:prose-invert
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

::ul{#menu.not-prose.flex-inline.flex-wrap.gap-3.w-full.text-sm.border-b-2.py-4.mt-2.mb-24.font-medium}

* [SK<i-fa7-solid-mountain align-text-bottom size-5/>LD](/)

* [Просто](/easy/)

* [Эффективно](/medium/)

* [Профессионально](/hard/)

* [ИИ](/ai/)

* [:span[]{.i-carbon-logo-github.align-middle.size-6}](https://github.com/skaldapp)

* <i-carbon-sun dark:i-carbon-moon align-middle size-6 dark:size-6 cursor-pointer @click="toggleDark()" />

::

<RouterView v-slot="{ Component }"><component :is="Component" v-if="Component" /><div v-else>

# SKALD{.text-center}

::ul{#download.not-prose.flex-inline.flex-wrap.gap-8.justify-center.w-full.my-24.font-medium}

* [:span[]{.i-material-icon-theme-folder-public-open.size-11.align-middle} webapp](https://skaldapp.github.io/skaldapp)

* [:span[]{.i-material-icon-theme-folder-windows-open.size-11.align-middle} windows](https://github.com/skaldapp/skaldapp/releases/latest)

* [:span[]{.i-material-icon-theme-folder-macos-open.size-11.align-middle} macos](https://github.com/skaldapp/skaldapp/releases/latest)

* [:span[]{.i-material-icon-theme-folder-linux-open.size-11.align-middle} appimage](https://github.com/skaldapp/skaldapp/releases/latest)

* [:span[]{.i-material-icon-theme-folder-snapcraft-open.size-11.align-middle} snap](https://snapcraft.io/skaldapp)

::

![1.00](uploads/mountain.svg "Мощный редактор для писателей и разработчиков с кристально чистым интерфейсом"){#mountain.not-prose.mb-24}

## Мощный редактор для писателей и разработчиков с кристально чистым интерфейсом

**Skald** – это инновационный текстовый редактор с поддержкой **Markdown**, созданный для тех, кто ценит **простоту, гибкость и безопасность** 🛡️✨. Он идеально подходит как для **писателей**, так и для **разработчиков**, предлагая **чистый и интуитивно понятный интерфейс**, который помогает сосредоточиться на главном – **творчестве и продуктивности** 🚀📝.

## 🚀 Ваш личный помощник 🤖 Интеграция с искусственным интеллектом

* Skald может стать вашим **личным помощником** 🤖✨:

  * Генерация идей и креативного контента.

  * Редактирование и улучшение текстов.

  * Автоматическое создание контента по заданным параметрам.

![1.00](uploads/light.png){#light.my-24}

![1.00](uploads/dark.png){#dark.my-24}

## 🌟 Уровни функциональности 🌟 {.text-center}

::ul{#levels.not-prose.flex-inline.flex-wrap.gap-x-8.gap-y-24.justify-center.w-full.my-24.text-center}

* ![1.00](uploads/emerald.png){#emerald.drop-shadow-2xl.drop-shadow-emerald-500/20}

  :::elCard{.h-full.pt-18.max-w-sm shadow="hover"}

  #header

  **ПРОСТОЙ**{.text-[var(--nord14)]}

  ● {.text-[var(--nord14)]}

  #default

  * древовидные заметки с поддержкой **markdown**

  * визуальный редактор с **wysiwyg** режимом

  * идеально подходит для **заметок, статей, документации и книг**

  #footer

  :elButton[ПРОСТОЙ ПРИМЕР]{type="success" size="large" tag="RouterLink" to="#simple"}

  :::

* ![1.00](uploads/ruby.png){#ruby.drop-shadow-2xl.drop-shadow-red-500/20}

  :::elCard{.h-full.pt-18.max-w-sm shadow="hover"}

  #header

  **ПРОДВИНУТЫЙ**{.text-[var(--nord11)]}

  ● {.text-[var(--nord11)]}

  #default

  * поддержка **html и tailwindcss** для создания стильных и современных страниц

  * **frontmatter** для управления метаданными и настройками страницы

  * ваши заметки превратятся в **красивый веб-ресурс** с удобной навигацией и адаптивным дизайном

  #footer

  :elButton[ПРОДВИНУТЫЙ ПРИМЕР]{type="danger" size="large" tag="RouterLink" to="#advanced"}

  :::

* ![1.00](uploads/diamond.png){#diamond.drop-shadow-2xl.drop-shadow-blue-500/20}

  :::elCard{.h-full.pt-18.max-w-sm shadow="hover"}

  #header

  **ПРОФЕССИОНАЛЬНЫЙ**{.text-[var(--nord10)]}

  ● {.text-[var(--nord10)]}

  #default

  * реактивность и управление динамическими данными с помощью **vue**

  * интеграция **сторонних библиотек** для расширения функциональности

  * разработка **сложных веб-приложений** прямо в редакторе

  #footer

  :elButton[ПРОФЕССИОНАЛЬНЫЙ ПРИМЕР]{type="primary" size="large" tag="RouterLink" to="#professional"}

  :::

::

### Простой пример{#simple}

::elTabs{tab-position="left"}

:::elTabPane{label="Результат"}

::::elCard

**Известные скальды:**

* Браги Боддасон (IX век) — один из первых известных скальдов, автор “Рагнардрапы” (поэмы о легендарном герое Рагнаре Лодброке).

* Эгиль Скаллагримссон (X век) — знаменитый воин и поэт, герой саги “Сага об Эгиле”.

* Снорри Стурлусон (XIII век) — автор “Младшей Эдды”, где подробно описаны правила скальдической поэзии.

::::

:::

:::elTabPane{.not-prose label="Исходный код"}

```markdown
**Известные скальды:**

* Браги Боддасон (IX век) — один из первых известных скальдов, автор “Рагнардрапы” (поэмы о легендарном герое Рагнаре Лодброке).

* Эгиль Скаллагримссон (X век) — знаменитый воин и поэт, герой саги “Сага об Эгиле”.

* Снорри Стурлусон (XIII век) — автор “Младшей Эдды”, где подробно описаны правила скальдической поэзии.
```

:::

::

### Продвинутый пример{#advanced}

::elTabs{tab-position="left"}

:::elTabPane{label="Результат"}

::::elCard

**Известные скальды:**

* Браги Боддасон (IX век) — один из первых известных скальдов, автор “Рагнардрапы” (поэмы о легендарном герое Рагнаре Лодброке).

* Эгиль Скаллагримссон (X век) — знаменитый воин и поэт, герой саги “Сага об Эгиле”.

* Снорри Стурлусон (XIII век) — автор “Младшей Эдды”, где подробно описаны правила скальдической поэзии.

::::

:::

:::elTabPane{.not-prose label="Исходный код"}

```markdown
**Известные скальды:**

* Браги Боддасон (IX век) — один из первых известных скальдов, автор “Рагнардрапы” (поэмы о легендарном герое Рагнаре Лодброке).

* Эгиль Скаллагримссон (X век) — знаменитый воин и поэт, герой саги “Сага об Эгиле”.

* Снорри Стурлусон (XIII век) — автор “Младшей Эдды”, где подробно описаны правила скальдической поэзии.
```

:::

::

### Профессиональный пример{#professional}

<elTabs tab-position="left">

<elTabPane label="Результат">
<elCard class="not-prose">

::form{@submit.prevent="addTodo"}
:::elInput{v-model="newTodo" required placeholder="new todo"}
#append
:elButton[Добавить задачу]{native-type="submit"}
:::
::
::ul{.my-2}
:::li{v-for="todo in filteredTodos" :key="todo.id"}
::::elInput{readonly :class="{ done: todo.done }" v-model="todo.text"}
#prepend
:elCheckbox{v-model="todo.done"}
#append
:elButton[X]{@click="removeTodo(todo)"}
::::
:::
::
:elButton[{{ hideCompleted ? "Показать все" : "Скрыть выполненные" }}]{@click="hideCompleted = !hideCompleted"}

</elCard>

</elTabPane>

<elTabPane class="not-prose text-sm" label="Исходный код">

```Markdown
---
script:
  - type: importmap
    innerHTML: |
      {
        "imports": {
          "element-plus": "https://cdn.jsdelivr.net/npm/element-plus@2/dist/index.full.min.mjs"
        }
      }
---

::form{@submit.prevent="addTodo"}
:::elInput{v-model="newTodo" required placeholder="new todo"}
#append
:elButton[Добавить задачу]{native-type="submit"}
:::
::
::ul{.my-2}
:::li{v-for="todo in filteredTodos" :key="todo.id"}
::::elInput{readonly :class="{ done: todo.done }" v-model="todo.text"}
#prepend
:elCheckbox{v-model="todo.done"}
#append
:elButton[X]{@click="removeTodo(todo)"}
::::
:::
::
:elButton[{{ hideCompleted ? "Показать все" : "Скрыть выполненные" }}]{@click="hideCompleted = !hideCompleted"}

<script setup>
import { getCurrentInstance, ref, computed } from 'vue'
import ElementPlus from 'element-plus'

const { appContext: { app } } = getCurrentInstance()
app.use(ElementPlus)

let id = 0

const newTodo = ref('')
const hideCompleted = ref(false)
const todos = ref([
  { id: id++, text: 'Изучить HTML', done: true },
  { id: id++, text: 'Изучить JavaScript', done: true },
  { id: id++, text: 'Изучить Vue', done: false }
])

const filteredTodos = computed(() => {
  return hideCompleted.value
    ? todos.value.filter((t) => !t.done)
    : todos.value
})

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value, done: false })
  newTodo.value = ''
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}
</script>

<style>
@import url("https://cdn.jsdelivr.net/npm/element-plus@2/dist/index.css");

.done {
  text-decoration: line-through;
}
</style>
```

</elTabPane>

</elTabs>

***

### 🚀 Готовы попробовать Skald?

Начните творить, создавать и развивать свои проекты **уже сегодня**! Skald – это ваш **надежный спутник** в мире текстов и веб-разработки 🌍💖.

</div></RouterView>

<script setup lang="ts">
import { getCurrentInstance, ref, computed } from "vue";
import ElementPlus from "element-plus";
import { useDark, useToggle } from "@vueuse/core";

const toggleDark = useToggle(useDark());
const { appContext: { app } } = getCurrentInstance();
app.use(ElementPlus);

let id = 0

const newTodo = ref('')
const hideCompleted = ref(false)
const todos = ref([
  { id: id++, text: 'Изучить HTML', done: true },
  { id: id++, text: 'Изучить JavaScript', done: true },
  { id: id++, text: 'Изучить Vue', done: false }
])

const filteredTodos = computed(() => {
  return hideCompleted.value
    ? todos.value.filter((t) => !t.done)
    : todos.value
})

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value, done: false })
  newTodo.value = ''
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}
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
.done {
  text-decoration: line-through;
}

body {
  @apply dark:bg-[var(--nord0)];
}

html:not(.dark) #dark,
html.dark #light {
  display: none !important;
}
</style>

<style scoped lang="postcss">
#menu {
  @apply border-[var(--nord8)];
}

#menu li:nth-last-child(2) {
  @apply ml-auto -mr-4;
}


#menu a.router-link-exact-active {
  @apply bg-[var(--nord8)] text-[var(--nord6)];
}

#levels>li {
  @apply relative;
}

#levels .el-card__body li {
  @apply my-6;
}

#levels img {
  @apply "absolute top-0 left-1/2 block w-32 -translate-x-1/2 -translate-y-1/2 hover:-translate-y-2/3 transition-transform duration-700";
}

#levels figcaption {
  @apply "text-center font-bold text-xl mb-4 uppercase after:content-['●'] after:block after:my-4";
}

#download a {
  @apply "border-2 transition hover:text-[var(--nord10)] rounded-md p-4 hover:bg-[var(--nord5)] whitespace-nowrap";
}

#mountain {
  @apply "dark:invert";
}

#menu a {
  @apply 'text-[var(--nord0)] transition hover:text-[var(--nord10)] px-3 py-2 rounded-md dark:text-[var(--nord6)]';
}
</style>
