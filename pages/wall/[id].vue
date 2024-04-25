<template>
  <div class="flex flex-col gap-4">
    <div class="relative right-1 top-1 border-2 border-dark bg-white rounded-lg">
      <div class="relative left-1 bottom-1  border-2 border-dark bg-white rounded-lg flex">
        <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="object-cover w-20 rounded-l-lg border-r-2 border-dark">
        <div class="flex gap-2 items-center grow justify-between px-4 py-3">
          <div class="">
            <h2 class="font-bold">阿爾敏</h2>
            <div>987,987 人追蹤</div>
          </div>
          <!-- <button class="h-9 px-3 sm:px-8 btn-3d-bright">追蹤</button> -->
          <button class="h-9 px-3 sm:px-8 btn-3d-gray">取消追蹤</button>
        </div>
      </div>
    </div>

    <Searchbar />
    <div class="p-6 bg-white border-2 border-dark rounded-lg text-dark-gray">目前尚無動態，新增一則貼文吧！</div>

    <Post />
  </div>
</template>
