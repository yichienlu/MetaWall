<template>
  <div>
    <div>
      <div class="relative right-1 top-1 border-2 border-dark bg-white">
        <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">我按讚的貼文</div>
      </div>
    </div>
    <ul class="mt-4 flex flex-col gap-4">
      <li class="flex gap-4 items-center p-4 bg-white rounded-lg border-2 border-dark border-b-4 font-bold">
        <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="object-cover w-10 h-10 rounded-full">
        <div class="grow">
          <h2 class="bolck hover:text-primary">愛爾敏</h2>
          <div class="text-dark-gray text-sm font-normal">發文時間：2022/1/10 12:00</div>
        </div>
        <button class="block sm:mr-9 ml-auto">
          <Icon name="material-symbols:thumb-up-outline" class="w-6 h-6 text-primary" />
          <p>取消</p>
        </button>
        <button class="block sm:mr-9 ">
          <Icon name="icons8:right-round" class="w-6 h-6 text-primary" />
          <p>查看</p>
        </button>
      </li>
      
    </ul>
  </div>
</template>
