
<template>
  <div class="bg-grid min-h-dvh relative pb-24">
    <Header />
    <div class="px-4 pt-12">
      <div class="container grid md:grid-cols-3 gap-4">
        <div  class="col-span-2">
        <slot />

        </div>
        <Menu class="fixed bottom-4 left-0 md:relative md:bottom-auto" />
      </div>
    </div>

  </div>
</template>
<style>
.bg-grid {
  background-color: theme("colors.background");
  background-image: linear-gradient(theme("colors.background-grid") 1px, transparent 1px), 
  linear-gradient(to right, theme("colors.background-grid") 1px, theme("colors.background") 1px);
  background-size: 50px 50px;
}
</style>