---
title: Vue
attrs:
  un-cloak: true
  class:
    - w-full
icon: twemoji:page-facing-up
---

## Шаблонизация

### Интерполяция

Каждый файл Markdown сначала компилируется в HTML, а затем передается в качестве компонента Vue в конвейер процесса. Это означает, что вы можете использовать интерполяцию в стиле Vue в тексте:

**Разметка**

::pre

[{{ 1 + 1 }}]{v-pre}

::

::elCard{header="Результат" header-class="font-bold"}

#default
{{ 1 + 1 }}

::

### Директивы

Директивы также работают (обратите внимание, что по замыслу необработанный HTML также допустим в Markdown):

**Разметка**

::div{v-pre}

```html

<span v-for="i in 3">{{ i }}</span>

```

::

::elCard{header="Результат" header-class="font-bold"}

<span v-for="i in 3">{{ i }}</span>

::

## `<script>` и `<style>`

Теги корневого уровня `<script>` и `<style>` в Markdown-файлах работают так же, как и в Vue SFC, включая `<script setup>`, `<style module>` и т. д. Главное отличие заключается в отсутствии тега `<template>`: всё остальное содержимое корневого уровня — Markdown. Также обратите внимание, что все теги должны располагаться **после** метаданных:

::div{v-pre}

```Markdown

---
title: hello world
---

<script setup>
import { ref } from "vue";

const count = ref(0);
</script>

## Содержание в формате Markdown. Счётчик: {{ count }}

<button class="button" @click="count++">Увеличить</button>

<style scoped>
.button {
  color: red;
  font-weight: bold;
}
</style>
```

::

## Использование компонентов

Вы можете импортировать и использовать компоненты Vue непосредственно в файлах Markdown.

:elAlert{.not-prose title="Библиотеки по умолчанию" type="warning" description="Библиотеки vue и vue-router входят в сборку по умолчанию, поэтому их не нужно указывать в `importmap`." show-icon :closable="false"}

<br />

:elAlert{.not-prose title="Модули" type="primary" description="В современных пакетах обычно уже присутствует файл esm модуля для подключения. Если по какой-либо причине в пакете нет esm модуля, то можно воспользоваться сервисами, которые соберут для вас модуль из исходников пакета: <https://esm.sh>, <https://esm.run>" show-icon :closable="false"}

### Импорт в Markdown

Если компонент используется только на нескольких страницах, рекомендуется явно импортировать его туда, где он используется. Это позволяет правильно разделить их по коду и загружать только при показе соответствующих страниц. Не забывайте использовать `importmap` при импорте компонентов из CDN.

```Markdown
---
title: Использование компонентов
script:
  - type: importmap
    innerHTML: |
      {
        "imports": {
          "element-plus": "https://cdn.jsdelivr.net/npm/element-plus@2/dist/index.full.min.mjs"
        }
      }
---

<script setup>
import { ref } from "vue";
import { elRate } from "element-plus";

const value = ref(3.7);
</script>

<style scoped src="https://cdn.jsdelivr.net/npm/element-plus@2/theme-chalk/index.css"></style>
<style scoped src="https://cdn.jsdelivr.net/npm/element-plus@2/theme-chalk/dark/css-vars.css"></style>

# Документация

Это .md с использованием пользовательского компонента

<elRate v-model="value" disabled show-score text-color="#ff9900" score-template="{value} points" />

## Другая документация

...
```

<elCard header="Результат" header-class="font-bold">

# Документация

Это .md с использованием пользовательского компонента

<elRate v-model="value" disabled show-score text-color="#ff9900" score-template="{value} points" />

## Другая документация

...

</elCard>

Если же необходимо определить компоненты глобально, то можно использовать экземпляр приложения `window.__vue_app__` и зарегистрировать компоненты в нем.

```Markdown

---
title: Использование компонентов
script:
  - type: importmap
    innerHTML: |
      {
        "imports": {
          "element-plus": "https://cdn.jsdelivr.net/npm/element-plus@2/dist/index.full.min.mjs"
        }
      }
---

<script setup>
import { ref } from "vue";
import ElementPlus from "element-plus";

const app = window.__vue_app__;
app.use(ElementPlus);

const value = ref(3.7);
</script>

<style>
@import url("https://cdn.jsdelivr.net/npm/element-plus@2/theme-chalk/index.css");
@import url("https://cdn.jsdelivr.net/npm/element-plus@2/theme-chalk/dark/css-vars.css");
</style>

# Документация

Это .md с использованием пользовательского компонента

<elRate v-model="value" disabled show-score text-color="#ff9900" score-template="{value} points" />

## Другая документация

...

```

## Роутинг

Для использования роутинга необходимо включить параметр template: true в конфигурации страницы и добавить таг <RouterView /> в шаблон страницы. Это позволит отображать дочерние страницы внутри родительской страницы.

:elAlert{.not-prose title="Наследование метаданных" type="primary" description="Дочерние страницы наследуют метаданные от родительских шаблонных страниц. К примеру, если в родительской шаблонной странице указан importmap, то он будет доступен и в дочерних страницах." show-icon :closable="false"}

```Markdown
---
title: Родительская страница
template: true
---

# Родительская страница

<RouterView />

```

Хотя в проекте сколько угодно страниц могут содержать таг `<RouterView />`, хорошей идеей является использовать его в корневой странице, назначив ей параметр template: true. Это позволит отображать дочерние страницы внутри родительской страницы, использовать общий шаблон для всех страниц, а также использовать метаданные родительской страницы в дочерних страницах.

<script setup>
import { ref } from "vue";

const value = ref(3.7);
</script>
