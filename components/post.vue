<script setup>
const props = defineProps({
  post: {
    type: Object,
    required: true,
  },
});
const { post } = props;


let liked = ref(false)
</script>
<template>
  <div class="bg-white rounded-lg p-6 border-2 border-dark shadow-[0_3px_0_0_#000400]">
    <div class="flex">
      <NuxtLink :to="`/wall/${post.userId}`">
        <img :src="post.userImg" alt="" class="object-cover w-12 h-12 rounded-full mr-4 border-2 border-dark hover:border-primary">
      </NuxtLink>
      <div>
        <NuxtLink :to="`/wall/${post.userId}`" class="font-bold hover:text-primary">{{ post.name }}</NuxtLink>
        <NuxtLink :to="`/post/${post.id}`">
          <div class="text-12 text-dark-gray hover:underline" v-timeformat="post.createdAt*1000"></div>
        </NuxtLink>
      </div>
    </div>
    <div class="mt-4" v-html="post.content"></div>
    <img :src="post.postImg" alt="" class="max-w-full mt-4 rounded-lg border-2 border-dark">
    <div class="flex mt-4 items-center">
      <button class=" text-dark-gray hover:text-dark" :class="{'text-primary':post.liked}"><Icon name="material-symbols:thumb-up-outline" class="w-6 h-6 " /></button>
      <div class="px-2 text-dark-gray" v-if="post.likes==0">成為第一個按讚的朋友</div>
      <div v-else class="px-2 relative group">{{ post.likes.length }}
        <div class="absolute bottom-full hidden group-hover:block w-40 max-h-40 overflow-y-auto p-2 bg-white border-2 border-dark">
          <ul class="text-xs">
            <li v-for="item in post.likes" :key="item.userId"><NuxtLink :to="`/wall/${item.userId}`" class="block py-1 truncate ">{{ item.name }}</NuxtLink></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="flex items-center gap-2 mt-4">
      <img :src="post.userImg" alt="" class="hidden md:block object-cover w-10 h-10 rounded-full border-2 border-dark">
      <div class="flex grow border-2 border-dark">
        <input type="text" class="grow shrink px-4 w-3/4" placeholder="留言">
        <button class="w-1/4 px-3 sm:px-6 lg:px-12 btn-input h-10 shrink">留言</button>
      </div>
    </div>
    <ul class="mt-4 flex flex-col gap-4" v-for="comment in post.comments" :key="comment?.id">
      <li class="p-4 rounded-xl bg-background flex gap-3">
        <NuxtLink :to="`/wall/${comment?.userId}`">
          <img :src="comment?.userImg" alt="" class="object-cover w-10 h-10 rounded-full border-2 border-dark hover:border-primary">
        </NuxtLink>
        <div>
            <NuxtLink :to="`/wall/${comment?.userId}`" class="hover:text-primary">{{ comment?.name }}</NuxtLink>
          <div class="text-12 text-dark-gray" v-timeformat="comment?.createdAt*1000"></div>
          <div class="mt-1">{{ comment?.comment }}</div>
        </div>
      </li>
    </ul>
  </div>
</template>