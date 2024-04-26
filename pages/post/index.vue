<script>
  useHead({
    title: "張貼動態"
  })
</script>
<template>
  <div>
    <!-- <Titlebox /> -->
    <div class="relative right-1 top-1 border-2 border-dark bg-white">
      <div class="relative left-1 bottom-1 py-4 border-2 border-dark bg-white text-center text-xl font-bold">張貼動態</div>
    </div>
    <div class="p-8 rounded-lg border-2 border-dark bg-white mt-4">
      <label for="postTextarea" class="block mb-1">貼文內容</label>
      <textarea name="" id="postTextarea" cols="30" rows="10" class="block w-full border-2 border-dark px-4 py-3" placeholder="輸入您的貼文內容"></textarea>
      <div class="my-4"><button class="py-1 px-8 rounded  btn-2d-dark">上傳圖片</button></div>
      <div class="mb-8"><img src="https://picsum.photos/1050/300" alt="" class="rounded-lg border-2 border-dark"></div>
      <ul class="mb-4 text-center text-danger text-sm">
        <li>圖片檔案過大，僅限 1mb 以下檔案</li>
        <li>圖片格式錯誤，僅限 JPG、PNG 圖片</li>
      </ul>
      <div>
        <button class="w-[323px] btn-3d block mx-auto ">送出貼文</button>
      </div>
    </div>
  </div>
</template>
