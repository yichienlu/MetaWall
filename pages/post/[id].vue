<script setup>
const post = {
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
}

useHead({
    title: `${post.name}`
  })
</script>

<template>
  <div>
    <Post :post="post" />
  </div>
</template>
