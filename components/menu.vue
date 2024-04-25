<template>
  <div class=" w-full px-2 md:px-0 font-bold">
    <div class="flex md:flex-col justify-center  py-2 bg-background md:bg-white rounded-full md:rounded-none border-2 border-dark gap-6 md:px-6 md:py-8">
      <NuxtLink to="/wall/123" class="flex items-center gap-4 md:px-2 md:order-2 group">
        <span class="flex justify-center items-center h-12 w-12 rounded-full border-2 border-dark bg-cover bg-center group-hover:bg-primary group-hover:text-white group-hover:border-primary" style="background-image:url('https://randomuser.me/api/portraits/men/15.jpg')"></span>
        <span class="hidden md:block group-hover:text-primary">邊緣小杰</span>
      </NuxtLink>
      <NuxtLink to="/following" class="flex items-center gap-4 md:px-2 md:order-3 group">
        <span class="flex justify-center items-center h-12 w-12 rounded-full border-2 border-dark bg-white group-hover:bg-primary group-hover:text-white group-hover:border-primary"><Icon name="uil:bell" class="w-6 h-6 " /></span>
        <span class="hidden md:block group-hover:text-primary">追蹤名單</span>
      </NuxtLink>
      <NuxtLink to="/likes" class="flex items-center gap-4 md:px-2 md:order-4 group">
        <span class="flex justify-center items-center h-12 w-12 rounded-full border-2 border-dark group-hover:bg-primary bg-white group-hover:text-white group-hover:border-primary"><Icon name="material-symbols:thumb-up-outline" class="w-6 h-6 " /></span>
        <span class="hidden md:block group-hover:text-primary">我按讚的文章</span>
      </NuxtLink>
      <NuxtLink to="/post" class="flex items-center justify-center md:order-1">
        <span class="flex md:hidden justify-center items-center h-12 w-12 rounded-full bg-primary hover:bg-bright text-white hover:text-dark border-2 border-dark"><Icon name="ic:round-plus" class="w-6 h-6" /></span>
        <span class="hidden md:block btn-3d w-full text-center">張貼動態</span>
      </NuxtLink>
    </div>

  </div>
</template>