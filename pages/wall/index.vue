<script setup>
  useHead({
    title:"貼文牆"
  })
  const posts = [
  {
      id:"123",
      userId:"123",
      name:"邊緣小杰",
      userImg:"https://randomuser.me/api/portraits/men/15.jpg",
      createdAt:1700000000,
      content:"<p>外面看起來就超冷....</p><p>我決定回被窩繼續睡....</p>",
      postImg:"https://picsum.photos/500/300",
      likes:12,
      liked:true,
      comments:[
        {
          id:"456",
          userImg:"https://picsum.photos/100/200",
          userId:"456",
          name:"希琳",
          createdAt:1700000000,
          comment:"真的～我已經準備冬眠了"
        },
        {
          id:"789",
          userImg:"https://randomuser.me/api/portraits/men/1.jpg",
          userId:"789",
          name:"波吉",
          createdAt:1700000000,
          comment:"會嗎？我沒穿衣服都不覺得冷"
        }
      ]
    },
    {
      id:"000",
      userId:"000",
      name:"米卡莎",
      userImg:"https://randomuser.me/api/portraits/women/15.jpg",
      createdAt:1700090000,
      content:"<p>搶到想要的 NFT 啦！ya~~</p>",
      postImg:"https://picsum.photos/400/300",
      likes:0,
      liked:false,
      comments:[
      ]
    }
  ]
</script>
<template>
  <div>
    <Searchbar />
    <ul v-if="posts.length" class="mt-4 flex flex-col gap-4">
      <li v-for="post in posts" :key="post.id">
        <Post :post="post" />
      </li>
    </ul>
    <div v-else class="p-6 mt-4 bg-white border-2 border-dark rounded-lg text-dark-gray">目前尚無動態，<nuxt-link to="/post" class="underline underline-dark underline-2 underline-offset-2 text-dark hover:text-primary font-bold">新增</nuxt-link>一則貼文吧！</div>
  </div>
</template>