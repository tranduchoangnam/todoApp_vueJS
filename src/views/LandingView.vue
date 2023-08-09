<script setup lang="ts">
import Header from '../components/Header.vue'
import Card from '../components/Card.vue'
</script>

<template>
  <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet" />
  <main>
    <div class="flex justify-center h-screen relative">
      <Header />
      <img
        src="../assets/images/Rectangle.png"
        alt="rectangle"
        class="hidden lg:flex w-[20rem] h-[20rem] absolute left-[5%] top-[40%]"
      />
      <img
        src="../assets/images/Rectangle-2.png"
        alt="rectangle"
        class="hidden lg:flex w-[18rem] h-[18rem] absolute right-[5%] top-[10%]"
      />
      <div class="relative h-[17rem] mt-[8rem] col text-center font-mono">
        <img
          src="../assets/images/success.png"
          alt="rectangle"
          class="w-[8rem] h-[8rem] float-center"
        />
        <p class="text-[3rem] font-bold mb-4">Turning Tasks into Triumphs.</p>
        <p>
          TodoApp: Your Journey to Task Mastery Begins Here.<br />
          Embrace organization, seize productivity, and create your success story.
        </p>
        <img
          src="../assets/images/Icon.png"
          alt="rectangle"
          class="absolute bottom-0 right-0 w-[4rem] h-[4rem]"
        />
        <div class="w-full mt-[8rem] flex justify-center">
          <div
            class="cursor-pointer w-[10rem] text-[1rem] font-bold text-white h-[4rem] flex justify-center items-center rounded-full bg-[var(--color-button)] px-3 py-1"
          >
            Start now
          </div>
        </div>
      </div>
    </div>
    <div class="pt-[5rem] font-mono justify-center min-h-screen relative col">
      <div class="col mb-14 text-center">
        <p class="text-3xl text-[var(--color-button)]">How it works</p>
        <p class="text-3xl font-bold font-sans">Simple steps to make a todo list</p>
      </div>
      <div class="flex flex-wrap justify-evenly">
        <Card>
          <template #header>
            <img src="../assets/images/Icon-2.png" alt="icon" class="w-[4rem] h-[4rem]" />
          </template>

          <template #default>
            <p class="font-bold">Register your account</p>
          </template>
          <template #detail>
            <p>Create a user account to access all the features of TodoApp.</p>
          </template>
        </Card>
        <Card>
          <template #header>
            <img src="../assets/images/Icon-3.png" alt="icon" class="w-[4rem] h-[4rem]" />
          </template>

          <template #default>
            <p class="font-bold">Add a todo</p>
          </template>
          <template #detail>
            <p>Click the add button to add a new todo.</p>
          </template>
        </Card>
        <Card>
          <template #header>
            <img src="../assets/images/Icon-4.png" alt="icon" class="w-[4rem] h-[4rem]" />
          </template>

          <template #default>
            <p class="font-bold">Check if completed</p>
          </template>
          <template #detail>
            <p>Click the checkbox to mark a todo as completed.</p>
          </template>
        </Card>
      </div>
    </div>
  </main>
</template>
