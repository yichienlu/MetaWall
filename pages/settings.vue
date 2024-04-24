<script setup>
const nameTab = ref(true)
const toggleTab = () => { nameTab.value = !nameTab.value }
</script>
<template>
  <div>
    <div class="relative right-1 top-1 border-2 border-dark bg-white">
      <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">修改個人資料
      </div>
    </div>
    <div class="mt-8">
      <div class="flex pl-4">
        <button class="px-6 py-2 rounded-t-lg bg-white border-2 border-b-0 border-dark"
          :class="{ 'bg-dark text-white': nameTab }" @click="toggleTab">暱稱修改</button>
        <button class="px-6 py-2 rounded-t-lg bg-white border-2 border-b-0 border-dark"
          :class="{ 'bg-dark text-white': !nameTab }" @click="toggleTab">重設密碼</button>
      </div>
      <div class="py-8 px-4 bg-white rounded-lg border-2 border-dark">
        <div v-if="nameTab" class="max-w-[323px] w-full mx-auto flex flex-col items-center gap-4">
          <img src="https://images.unsplash.com/photo-1554629947-334ff61d85dc?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8" alt="" class="object-cover  w-28 h-28 rounded-full border-2 border-dark">

          <button class="py-2 px-6 bg-dark text-white">上傳大頭照</button>

          <div class="w-full">
            <label for="" class="mb-1">暱稱</label>
            <input type="text" placeholder="請輸入暱稱" class="w-full h-12 px-6 border-2 border-dark">
          </div>

          <div class="w-full">
            <legend>性別</legend>
            <div class="flex items-center">
              <input type="radio" id="male" name="gender" class="appearance-none" checked />
              <Icon name="ic:baseline-radio-button-checked" class="text-dark w-6 h-6"></Icon>
              <label for="male" class="ml-3 mr-6">男性</label>
              <input type="radio" id="female" name="gender" class="appearance-none" />
              <Icon name="ic:baseline-radio-button-unchecked" class="text-dark w-6 h-6"></Icon>
              <label for="female" class="ml-3 mr-6">女性</label>
            </div>
          </div>

            <ol class="text-center text-danger text-sm mt-4">
              <li>1.圖片寬高比必需為 1:1，請重新輸入</li>
              <li>2. 解析度寬度至少 300像素以上，請重新輸入</li>
            </ol>

            <button
              class="block w-full py-4 bg-primary text-white font-bold rounded-lg border-2 border-dark shadow-[-2px_2px_0_0_#000400]">送出更新</button>
          
        </div>

        <div v-else class="max-w-[323px] w-full mx-auto">
          <form action="">
            <label for="" class="mb-1">輸入新密碼</label>
            <input type="text" class="w-full mb-4 px-6 h-12 border-2 border-dark" placeholder="請輸入新密碼">

            <label for="" class="mb-1">再次輸入</label>
            <input type="text" class="w-full mb-8 px-6 h-12 border-2 border-dark" placeholder="再次輸入新密碼">

            <button class="w-full py-4 bg-secondary text-white rounded-lg border-2 border-[#808080]">重設密碼</button>
          </form>

        </div>
      </div>
    </div>
  </div>
</template>
