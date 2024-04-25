<template>
  <div class="flex flex-col gap-4">
    <div class="relative right-1 top-1 border-2 border-dark bg-white rounded-lg">
      <div class="relative left-1 bottom-1  border-2 border-dark bg-white rounded-lg flex">
        <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="" class="object-cover w-20 h-20 rounded-l-lg border-r-2 border-dark">
        <div class="flex items-center grow justify-between px-4">
          <div>
            <h2 class="font-bold">阿爾敏</h2>
            <div>987,987 人追蹤</div>
          </div>
          <button class="h-9 px-8 rounded-lg bg-bright border-2 border-dark font-bold shadow-[0_2px_0_0_#000400]">追蹤</button>
        </div>
      </div>
    </div>

    <Searchbar />

    <Post />
  </div>
</template>
