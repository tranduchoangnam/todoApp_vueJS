<script setup lang="ts">
import Login from '../components/Login.vue'
import { ref } from 'vue'
const toggle = ref(false)
const toggleLogin = () => {
  toggle.value = !toggle.value
}
</script>

<template>
  <link
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
  />
  <div class="flex justify-between items-center bg-green-500 text-white h-12 px-4">
    <h1 class="text-2xl cursor-pointer">Todo App</h1>
    <div class="flex">
      <span
        @click="toggleLogin"
        class="inline-block justify-center cursor-pointer material-symbols-outlined"
      >
        person
      </span>
    </div>
  </div>
  <p>{{ toggle }}</p>
  <Login v-if="toggle" :toggleLogin="toggleLogin" />
</template>
