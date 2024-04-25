<script setup>
  const listOpen = ref(false)
  const toggleList = () => {
    listOpen.value = ! listOpen.value
  }

</script>
<template>
  <div class="bg-white border-b-2 border-dark px-3">
    <div class="container flex justify-between">
      <NuxtLink to="/wall" class="text-2xl sm:text-3xl flex items-center paytone">MetaWall</NuxtLink>
      <div class="relative ">
        <button class="flex py-3" @click="toggleList">
          <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="object-cover h-[30px] w-[30px] rounded-full border-2 border-black mr-2">
          <div class="p-1 border-b-2 border-dark text-base leading-5 paytone">Member</div>
        </button>
        <div class="absolute w-[182px] right-0 top-100 bg-white border-2 border-dark z-50" :class="{'hidden':!listOpen}">
          <ul class="relative right-2 bottom-2 bg-white border-2 border-dark text-center">
            <li class="border-b-2 border-dark py-2 hover:bg-background">
              <NuxtLink to="/wall" @click="toggleList">我的貼文牆</NuxtLink>
            </li>
            <li class="border-b-2 border-dark py-2 hover:bg-background">
              <NuxtLink to="/settings" @click="toggleList">修改個人資料</NuxtLink>
            </li>
            <li class="py-2 hover:bg-background" @click="toggleList">
              <NuxtLink to="/" @click="toggleList">登出</NuxtLink>
            </li>
          </ul>
        </div>
      </div>


    </div>
  </div>
</template>
