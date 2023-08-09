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
  <div class="flex absolute top-0 items-center h-[5rem] w-screen px-4">
    <h1 class="absolute left-[5%] text-[1rem] font-bold cursor-pointer">Todo App</h1>
    <div class="hidden md:flex absolute left-[50%] translate-x-[-50%]">
      <p class="cursor-pointer mr-7 text-[1rem] text-black">Get Started</p>
      <p class="cursor-pointer mr-7 text-[1rem] text-black">Feature</p>
      <p class="cursor-pointer mr-7 text-[1rem] text-black">About me</p>
    </div>
    <div class="absolute right-[5%] flex justify-around items-center float-right">
      <p class="cursor-pointer mr-5 text-[1rem] font-bold text-black" @click="toggleLogin">
        Log in
      </p>
      <!-- <span
        @click="toggleLogin"
        class="inline-block justify-center cursor-pointer material-symbols-outlined"
      >
        person
      </span> -->
      <div
        class="cursor-pointer w-[10rem] text-[1rem] font-bold text-white h-[4rem] flex justify-center items-center rounded-full bg-[var(--color-button)] px-3 py-1"
      >
        Create Account
      </div>
    </div>
  </div>
  <Login v-if="toggle" :toggleLogin="toggleLogin" />
</template>
