<script setup>
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
          name:"希琳",
          createdAt:1700000000,
          comment:"真的～我已經準備冬眠了"
        },
        {
          id:"789",
          userImg:"https://randomuser.me/api/portraits/men/1.jpg",
          name:"波吉",
          createdAt:1700000000,
          comment:"會嗎？我沒穿衣服都不覺得冷"
        }
      ]
    },
    {
      id:"123",
      userId:"123",
      name:"邊緣小杰",
      userImg:"https://randomuser.me/api/portraits/men/15.jpg",
      createdAt:1700000000,
      content:"<p>超冷</p>",
      postImg:"https://picsum.photos/300/300",
      likes:0,
      liked:false,
      comments:[
        {
          id:"456",
          userImg:"https://picsum.photos/200/100",
          name:"琳希",
          createdAt:1700000000,
          comment:"真的～"
        },
        {
          id:"789",
          userImg:"https://randomuser.me/api/portraits/men/18.jpg",
          name:"吉波",
          createdAt:1700000000,
          comment:"會嗎？"
        }
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