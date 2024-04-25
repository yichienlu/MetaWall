<script setup>
definePageMeta({
  layout: 'login'
})
const login = ref(true)
</script>

<template>
  <div>
    <h2 class="sm:text-2xl font-bold mb-4 sm:mb-9">
      <span v-if="login">到元宇宙展開全新社交圈</span>
      <span v-else>註冊</span>
    </h2>

    <div  v-if="login">
      <input type="email" class="w-full h-12 px-6 mt-4 border-2 border-dark" placeholder="Email">
      <input type="password" class="w-full h-12 px-6 mt-4 border-2 border-dark" placeholder="Password">
      <p class="text-danger mb-4 mt-8">帳號或密碼錯誤，請重新輸入！</p>
      <NuxtLink to="/wall">
        <button class="w-full h-12 mt-8 border-2 border-dark bg-primary text-white rounded-lg shadow-[-2px_2px_0_0_#000400]">登入</button>
      </NuxtLink>
    </div>
    <div v-else>
      <input type="text" class="w-full h-12 px-6 border-2 border-dark" placeholder="暱稱">
      <p class="text-danger text-start mt-1">暱稱至少 2 個字元以上</p>

      <input type="email" class="w-full h-12 px-6 mt-4 border-2 border-dark" placeholder="Email">
      <p class="text-danger text-start mt-1">暱稱至少 2 個字元以上</p>

      <input type="password" class="w-full h-12 px-6 mt-4 border-2 border-dark" placeholder="Password">
      <p class="text-danger text-start mt-1">暱稱至少 2 個字元以上</p>

      <NuxtLink to="/wall">
        <button class="w-full h-12 mt-8 border-2 border-dark bg-primary text-white rounded-lg shadow-[-2px_2px_0_0_#000400]">登入</button>
      </NuxtLink>
    </div>
    <div class="mt-4">
      
        <button @click="login = !login">
          <span v-if="login">註冊帳號</span>
          <span v-else>登入</span>
        </button>
    </div>
  </div>

</template>