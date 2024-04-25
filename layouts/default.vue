
<template>
  <div class="bg-grid min-h-dvh relative pb-24">
    <Header class="sticky top-0 z-20" />
    
    <div class="px-4 pt-12">
      <div class="container grid md:grid-cols-3 gap-4">
        <div  class="col-span-2">
        <slot />

        </div>
        <div class="relative">
          <Menu class="fixed bottom-4 left-0 md:sticky md:top-[104px] md:bottom-auto" />
        </div>
      </div>
    </div>

  </div>
</template>
<style>

</style>