<script setup>

</script>
<template>
  <div class="bg-white rounded-lg p-6 border-2 border-dark shadow-[0_3px_0_0_#000400]">
    <div class="flex">
      <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="w-12 h-12 rounded-full mr-4 border-2 border-dark">
      <div>
        <div class="font-bold">邊緣小杰</div>
        <div class="text-12 text-dark-gray">2022/10/10 12:00</div>
      </div>
    </div>
    <div class="mt-4">
      <p>外面看起來就超冷....</p>
      <p>我決定回被窩繼續睡....>.<</p>
    </div>
    <img src="https://picsum.photos/500/300" alt="" class="object-fit mt-4">
    <div class="flex mt-4">
      <button><Icon name="material-symbols:thumb-up-outline" class="w-6 h-6 " /></button>
      <span class="ml-2">12</span>
    </div>
    <div class="flex items-center gap-2 mt-4">
      <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="w-10 h-10 rounded-full border-2 border-dark">
      <div class="flex grow border-2 border-dark">
        <input type="text" class="grow">
        <button class="px-12 bg-primary border-l-2 border-dark text-white h-10">留言</button>
      </div>
    </div>
    <ul class="mt-4 flex flex-col gap-4">
      <li class="p-4 rounded-xl bg-background flex gap-3">
        <img src="https://randomuser.me/api/portraits/women/15.jpg" alt="" class="w-10 h-10 rounded-full border-2 border-dark">
        <div>
          <div>希琳</div>
          <div class="text-12 text-dark-gray">2022/10/10/15:00</div>
          <div class="mt-1">真的～我已經準備冬眠了</div>
        </div>
      </li>
      <li class="p-4 rounded-xl bg-background flex gap-3">
        <img src="https://randomuser.me/api/portraits/men/1.jpg" alt="" class="w-10 h-10 rounded-full border-2 border-dark">
        <div>
          <div>波吉</div>
          <div class="text-12 text-dark-gray">2022/10/10/15:00</div>
          <div class="mt-1">會嗎？我沒穿衣服都不覺得冷</div>
        </div>
      </li>
    </ul>
  </div>
</template>