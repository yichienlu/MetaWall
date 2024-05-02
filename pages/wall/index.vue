<script setup>
  useHead({
    title:"貼文牆"
  })

const posts = ref([])


  const sortList = async (arr) =>{
    useFetch(`https://node-hw4.onrender.com/posts/?timeSort=${arr[0]}&q=${arr[1]}`)
      .then(res=>{
        posts.value = res.data.value.data
      })
  }

</script>
<template>
  <div>
    <Searchbar @test="test" @sortList="sortList" />
    <ul v-if="posts.length" class="mt-4 flex flex-col gap-4">
      <li v-for="post in posts" :key="post._id">
        <Post :post="post" />
      </li>
    </ul>
    <div v-else class="p-6 mt-4 bg-white border-2 border-dark rounded-lg text-dark-gray">目前尚無動態，<nuxt-link to="/post" class="underline underline-dark underline-2 underline-offset-2 text-dark hover:text-primary font-bold">新增</nuxt-link>一則貼文吧！</div>
  </div>
</template>