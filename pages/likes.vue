<script setup>
  const likes = [
    {
      id:"123",
      userId:"123",
      name:"邊緣小杰",
      userImg:"https://randomuser.me/api/portraits/men/15.jpg",
      postTime:1720000000
    }
  ]
</script>
<template>
  <div>
    <div>
      <div class="relative right-1 top-1 border-2 border-dark bg-white">
        <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">我按讚的貼文</div>
      </div>
    </div>
    <ul class="mt-4 flex flex-col gap-4">
      <li class="flex gap-4 items-center p-4 bg-white rounded-lg border-2 border-dark border-b-4 font-bold" v-for="like in likes" :key="like.id">
        <NuxtLink :to="`/wall/${like.userId}`">
          <img :src="like.userImg" alt="" class="object-cover w-10 h-10 rounded-full">
        </NuxtLink>
        <div class="grow">
          <NuxtLink :to="`/wall/${like.userId}`" class="hover:text-primary">{{ like.name }}</NuxtLink>
          <div class="text-dark-gray text-sm font-normal">發文時間：<span v-timeformat="like.postTime*1000"></span></div>
        </div>
        <button class="block sm:mr-9 ml-auto">
          <Icon name="material-symbols:thumb-up-outline" class="w-6 h-6 text-primary" />
          <p>取消</p>
        </button>
        <NuxtLink :to="`/post/${like.id}`">
          <button class="block sm:mr-9 ">
            <Icon name="icons8:right-round" class="w-6 h-6 text-primary" />
            <p>查看</p>
          </button>
        </NuxtLink>
      </li>
      
    </ul>
  </div>
</template>
