<script setup>
  useHead({
    title: "張貼動態"
  })

let tempPost = ref({
  user:"66332fd014aa392dbd88be87",
  content:"",
  image:"",
  likes:0
})

const addPost = async () => {
  await $fetch('https://node-hw4.onrender.com/posts/', {
    method: 'post',
    body: tempPost.value
  })
  .then((res)=>console.log(res))
  .catch((err)=>console.dir(err))
}


// const alerts = ref([
//   "圖片檔案過大，僅限 1mb 以下檔案",
//   "圖片格式錯誤，僅限 JPG、PNG 圖片"
// ])

</script>
<template>
  <div>
    <div class="relative right-1 top-1 border-2 border-dark bg-white">
      <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">張貼動態</div>
    </div>
    <div class="p-8 rounded-lg border-2 border-dark bg-white mt-4">
      <label for="postTextarea" class="block mb-1">貼文內容</label>
      <textarea name="" id="postTextarea" cols="30" rows="10" class="block w-full border-2 border-dark px-4 py-3" placeholder="輸入您的貼文內容" v-model="tempPost.content"></textarea>
      <div class="my-4">
        <!-- <button class="py-1 px-8 rounded  btn-2d-dark">上傳圖片</button> -->
        <input type="text" class="py-2 px-4 rounded border-2 border-dark w-full" placeholder="請輸入圖片 URL" v-model="tempPost.image">
      </div>
      <div class="mb-8" v-if="tempPost.image"><img  :src="tempPost.image" alt="" class="rounded-lg border-2 border-dark"></div>
      <ul class="mb-4 text-center text-danger text-sm">
        <!-- <li v-for="item in alerts" :key="item">{{ item }}</li> -->
        <li v-if="tempPost.image && !tempPost.image.startsWith('https://')">圖片網址須為 https 開頭</li>
      </ul>
      <div>
        <button class="w-[323px] btn-3d block mx-auto " @click="addPost" :disabled="!((tempPost.content && !tempPost.image) || (tempPost.content && tempPost.image.startsWith('https://')))">送出貼文</button>
      </div>
    </div>
  </div>
</template>
