<template>
  <div
    class="col relative h-[20rem] w-[15rem] overflow-hidden shadow-xl bg-[#FFFFFF] m-4 rounded-lg"
  >
    <header
      class="flex my-[3rem] mx-auto border rounded-full overflow-hidden w-[4rem] h-[4rem] justify-center items-center"
    >
      <slot name="header"></slot>
    </header>

    <main class="text-center">
      <slot></slot>
    </main>
    <div class="mt-5 p-2 text-center">
      <slot name="detail"></slot>
    </div>
  </div>
</template>
