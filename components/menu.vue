<template>
  <div class=" w-full px-2 md:px-0 font-bold">
    <div class="flex md:flex-col justify-center  py-2 bg-background md:bg-white rounded-full md:rounded-none border-2 border-dark gap-6 md:px-6 md:py-8">
      <NuxtLink to="/wall" class="flex items-center gap-4 md:px-2 md:order-2">
        <span class="flex justify-center items-center h-12 w-12 rounded-full border-2 border-dark bg-cover bg-center" style="background-image:url('https://randomuser.me/api/portraits/men/15.jpg')"></span>
        <span class="hidden md:block">邊緣小杰</span>
      </NuxtLink>
      <NuxtLink to="following" class="flex items-center gap-4 md:px-2 md:order-3">
        <span class="flex justify-center items-center h-12 w-12 rounded-full border-2 border-dark bg-white"><Icon name="uil:bell" class="w-6 h-6 " /></span>
        <span class="hidden md:block">追蹤名單</span>
      </NuxtLink>
      <NuxtLink to="/likes" class="flex items-center gap-4 md:px-2 md:order-4 ">
        <span class="flex justify-center items-center h-12 w-12 rounded-full border-2 border-dark bg-white"><Icon name="material-symbols:thumb-up-outline" class="w-6 h-6 " /></span>
        <span class="hidden md:block">我按讚的文章</span>
      </NuxtLink>
      <NuxtLink to="post" class="flex items-center justify-center md:bg-primary md:text-white md:border-2 border-dark md:py-4 rounded-lg md:order-1 md:shadow-[-2px_2px_0px_0px_#000400]">
        <span class="flex md:hidden justify-center items-center h-12 w-12 rounded-full bg-primary border-2 border-dark"><Icon name="ic:round-plus" class="w-6 h-6 text-white" /></span>
        <span class="hidden md:block">張貼動態</span>
      </NuxtLink>
    </div>

  </div>
</template>