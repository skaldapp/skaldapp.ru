---
title: Title
description: Description
icon: twemoji:page-facing-up
attrs:
  un-cloak: true
---

### Профессиональный пример{#professional}

<elTabs>

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

<script setup lang="ts">
import { ref, computed } from "vue";

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

<style lang="postcss">
.done {
  text-decoration: line-through;
}
</style>