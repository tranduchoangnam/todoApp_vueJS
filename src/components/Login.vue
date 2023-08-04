<script setup lang="ts">
defineProps<{
  toggleLogin: VoidFunction
}>()
</script>

<template>
  <link
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
  />
  <div class="fixed top-0 left-0 w-screen h-screen bg-black/50">
    <div class="flex justify-center items-center w-full h-full">
      <div class="bg-white w-96 h-96 rounded-lg">
        <div class="flex justify-between items-center bg-green-500 text-white h-12 px-4">
          <h1 class="text-2xl cursor-pointer">Todo App</h1>
          <div class="flex">
            <span
              @click="toggleLogin"
              class="inline-block justify-center cursor-pointer material-symbols-outlined"
            >
              close
            </span>
          </div>
        </div>
        <div class="flex justify-center items-center h-80">
          <form class="flex flex-col justify-center items-center">
            <input
              type="text"
              placeholder="Username"
              class="border border-gray-300 rounded-lg px-4 py-2 w-80 mb-4"
            />
            <input
              type="password"
              placeholder="Password"
              class="border border-gray-300 rounded-lg px-4 py-2 w-80 mb-4"
            />
            <button type="submit" class="bg-green-500 text-white px-4 py-2 rounded-lg w-80">
              Login
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>
