<template>
  <div>
    <div class="relative right-1 top-1 border-2 border-dark bg-white">
      <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">追蹤名單</div>
    </div>
    <ul class="mt-4 flex flex-col gap-4">
      <li class="flex gap-4 items-center p-4 bg-white rounded-lg border-2 border-dark border-b-4">
        <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="object-cover w-10 h-10 rounded-full">
        <div class="grow">
          <NuxtLink to="wall" class="bolck font-bold hover:text-primary hover:underline hover:underline-offset-2">愛爾敏</NuxtLink>
          <div class="flex justify-between text-sm flex-col sm:flex-row">
            <div class="text-dark-gray">追蹤時間：2022/1/10 12:00</div>
            <div>您已追蹤 90 天！</div>
          </div>
        </div>
      </li>
      
    </ul>
  </div>
</template>
