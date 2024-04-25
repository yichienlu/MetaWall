<template>
  <div class="min-h-dvh px-3 py-3 flex justify-center items-center bg-grid ">
    <div class="container border-2 border-dark bg-background shadow-[-8px_8px_0_0_#00040029] px-3 sm:px-12 py-3 sm:py-16 grid sm:grid-cols-2 sm:gap-x-4 lg:gap-x-12">
      <div class="hidden sm:flex items-center justify-center">
        <img src="C:/Users/Admin/Downloads/img.svg" alt="" class="h-full">
      </div>
      <div class="text-center">
        <h1 class="paytone text-4xl sm:text-6xl text-primary leading-normal">MetaWall</h1>
        <slot />
      </div>

    </div>

  </div>  

</template>

<style scoped>

</style>
