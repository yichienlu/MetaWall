<script setup>
  const emit = defineEmits(['sortList'])

  let order = 'dec'
  let content = ""
  emit('sortList', [order,content])
  
</script>
<template>
  <div class="flex flex-col md:flex-row gap-3 items-stretch">
    <select name="" id="orderSelect" class="orderSelect md:w-40 px-4 py-3 relative border-2 border-dark" v-model="order" @change="emit('sortList', [order,content])">
        <option value="dec">最新貼文</option>
        <option value="asc">最舊貼文</option>
    </select>
    <div class="grow border-2 border-dark">
      <div class="flex">
        <input type="text" class="grow px-4 py-3" placeholder="搜尋貼文" v-model="content">
        <button class="p-3 btn-input"><Icon name="ic:search" class="w-6 h-6" @click="emit('sortList',[order,content])"/></button>
      </div>
    </div>
  </div>
</template>
<style lang="scss">

</style>