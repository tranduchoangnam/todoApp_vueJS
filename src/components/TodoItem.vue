<script setup lang="ts">
defineProps<{
  todo: {
    id: number
    text: string
    done: boolean
  }
  removeTodo: Function
}>()
</script>
<template>
  <link
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
  />

  <div
    class="hover:border-l-lime-500 hover:border-4 select-none my-1 w-full flex items-center justify-between border"
  >
    <h3>{{ todo.text }}</h3>
    <span @click="removeTodo(todo)" class="material-symbols-outlined green cursor-pointer">
      close
    </span>
  </div>
</template>
<style scoped></style>
