<template>
  <div class="flex flex-col md:flex-row gap-3 items-stretch">
    <select name="" id="orderSelect" class="orderSelect md:w-40 px-4 py-3 relative border-2 border-dark">
        <option value="">最新貼文</option>
        <option value="">熱門貼文</option>
    </select>
    <div class="grow border-2 border-dark">
      <div class="flex">
        <input type="text" class="grow px-4 py-3" placeholder="搜尋貼文">
        <button class="p-3 btn-input"><Icon name="ic:search" class="w-6 h-6" /></button>
      </div>
    </div>
  </div>
</template>
<style lang="scss">

</style>