<script setup>
  useHead({
    title: "追蹤名單"
  })
const following = [
  {
    id:"123",
    userImg:"https://randomuser.me/api/portraits/men/15.jpg",
    name:"邊緣小杰",
    createdAt:1714100000
  },
  {
    id:"456",
    userImg:"https://picsum.photos/100/200",
    name:"希琳",
    createdAt:1714000000
  },
  {
    id:"789",
    userImg:"https://randomuser.me/api/portraits/men/1.jpg",
    name:"波吉",
    createdAt:1712000000
  }
]
</script>
<template>
  <div>
    <div class="relative right-1 top-1 border-2 border-dark bg-white">
      <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">追蹤名單</div>
    </div>
    <ul class="mt-4 flex flex-col gap-4">
      <li class="flex gap-4 items-center p-4 bg-white rounded-lg border-2 border-dark border-b-4" v-for="user in following" :key="user.id">
        <img :src="user.userImg" alt="" class="object-cover w-10 h-10 rounded-full">
        <div class="grow">
          <NuxtLink :to="`/wall`" class="bolck font-bold hover:text-primary hover:underline hover:underline-offset-2">{{ user.name }}</NuxtLink>
          <div class="flex justify-between text-sm flex-col sm:flex-row">
            <div class="text-dark-gray">追蹤時間：<span v-timeformat="user.createdAt *1000"></span></div>
            <div>您已追蹤 <span>{{ Math.floor((Date.now()/1000- user.createdAt)/(60*60*24))}}</span> 天！</div>
          </div>
        </div>
      </li>
      
    </ul>
  </div>
</template>
