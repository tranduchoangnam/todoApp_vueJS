<script setup lang="ts">
import TodoItem from './TodoItem.vue'
import { ref } from 'vue'
let id: number = 0
interface Todo {
  id: number
  text: string
  done: boolean
}
const todos = ref([
  { id: id++, text: 'Learn JavaScript', done: false },
  { id: id++, text: 'Learn Vue', done: false },
  { id: id++, text: 'Play around in JSFiddle', done: true },
  { id: id++, text: 'Build something awesome', done: true }
])
const newTodo = ref('')
const addTodo = () => {
  todos.value.push({
    id: id++,
    text: newTodo.value,
    done: false
  })
  newTodo.value = ''
}
const removeTodo = (todo: Todo) => {
  todos.value = todos.value.filter((t) => t !== todo)
}
</script>
<template>
  <div class="justify-center flex h-auto my-20">
    <div class="w-[300px] h-auto lg:w-[500px] px-2.5 border">
      <h1 class="text-green-600 text-xl">Todos</h1>
      <input
        v-model="newTodo"
        class="w-full h-12 border rounded-lg text-lg px-1"
        placeholder="What needs to be done?"
      />
      <button
        class="bg-green-500 text-white float-right rounded-lg border px-1 my-1"
        @click="addTodo"
      >
        Add Todo
      </button>
      <TodoItem v-for="todo in todos" :key="todo.id" :todo="todo" :removeTodo="removeTodo" />
    </div>
  </div>
</template>
