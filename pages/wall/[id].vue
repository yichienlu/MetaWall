<script setup>
const profile = {
  id:"123",
  name:"邊緣小杰",
  userImg:"https://randomuser.me/api/portraits/men/15.jpg",
  followers:87000,
  followed:true,
  posts:[
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
    }
  ]
}
</script>

<template>
  <div class="flex flex-col gap-4">
    <div class="relative right-1 top-1 border-2 border-dark bg-white rounded-lg">
      <div class="relative left-1 bottom-1  border-2 border-dark bg-white rounded-lg flex">
        <img :src="profile.userImg" alt="" class="object-cover w-20 rounded-l-lg border-r-2 border-dark">
        <div class="flex gap-2 items-center grow justify-between px-4 py-3">
          <div class="">
            <h2 class="font-bold">{{ profile.name }}</h2>
            <div>{{ profile.followers.toLocaleString() }} 人追蹤</div>
          </div>
          <button v-if="profile.followed" class="h-9 px-3 sm:px-8 btn-3d-gray">取消追蹤</button>
          <button v-else class="h-9 px-3 sm:px-8 btn-3d-bright">追蹤</button>
        </div>
      </div>
    </div>

    <Searchbar class="my-4" />
    <ul v-if="profile.posts.length" class="mt-4 flex flex-col gap-4">
      <li v-for="post in profile.posts" :key="post.id">
        <Post :post="post" />
      </li>
    </ul>
    <div v-else class="p-6 bg-white border-2 border-dark rounded-lg text-dark-gray">目前尚無動態，新增一則貼文吧！</div>

  </div>
</template>
