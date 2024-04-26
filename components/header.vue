<script setup>
  const user = {
    id:"123",
    name:"邊緣小杰",
    userImg:"https://randomuser.me/api/portraits/men/15.jpg"
  }

</script>
<template>
  <div class="bg-white border-b-2 border-dark px-3">
    <div class="container flex justify-between">
      <NuxtLink to="/wall" class="text-2xl sm:text-3xl flex items-center paytone">MetaWall</NuxtLink>
      <div class="relative group">
        <button class="flex py-3 group">
          <img :src="user.userImg" alt="" class="object-cover h-[30px] w-[30px] rounded-full border-2 border-black mr-2 group-hover:border-primary">
          <div class="p-1 border-b-2 border-dark text-base leading-5 paytone group-hover:text-primary group-hover:border-primary">Member</div>
        </button>
        <div class="hidden group-hover:block absolute w-[182px] right-0 top-100 bg-white border-2 border-dark z-50" >
          <ul class="relative right-2 bottom-2 bg-white border-2 border-dark text-center">
            <li>
              <NuxtLink to="/wall" class="block border-b-2 border-dark py-2 hover:bg-background">我的貼文牆</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/settings" class="block border-b-2 border-dark py-2 hover:bg-background">修改個人資料</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/" class="block py-2 hover:bg-background">登出</NuxtLink>
            </li>
          </ul>
        </div>
      </div>


    </div>
  </div>
</template>
