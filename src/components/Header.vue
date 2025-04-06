<script setup>
import { ref } from 'vue'

const showInputDropdown = ref(false)
const inputDropdown = [
  '全站', '3C', '周邊', '筆電', '通訊',
  '數位', '家電', '日用', '母嬰', '食品',
  '生活', '居家', '休閒', '保健', '美妝',
  '時尚', '書店'
]
</script>

<template>
  <div class="bg-main h-[172px]">
    <div class="bg-[#9e1d1d] h-[37px]">
      <div class="container h-full flex justify-between items-center">
        <div class="flex text-primary-text text-sm">
          <button class="px-2 cursor-pointer hover:text-primary-text-hover">比比昂日本購物</button>
          <div class="px-2 cursor-pointer hover:text-primary-text-hover">綜合服務</div>
        </div>
        <div class="flex text-primary-text text-sm">
          <button class="px-2 cursor-pointer hover:text-primary-text-hover">最近看過</button>
          <button class="px-2 cursor-pointer hover:text-primary-text-hover">購物車</button>
          <button class="px-2 cursor-pointer hover:text-primary-text-hover">我的訂單</button>
          <button class="px-2 cursor-pointer hover:text-primary-text-hover">顧客中心</button>
          <button class="px-2 cursor-pointer hover:text-primary-text-hover">下載 APP</button>
          <button class="cursor-pointer hover:text-primary-text-hover">登出</button>
        </div>
      </div>
    </div>

    <div class="container flex pt-4 pb-2">
      <img src="/images/c2aeb346-6b77-4a0b-bc96-f41e3d1be76d.gif" alt="" class="w-[142px] h-[60px]">
      <div class="relative px-7.5">
        <form class="flex items-center bg-[#fff] rounded-lg w-[540px] h-[45px]">
          <button @click="showInputDropdown = !showInputDropdown" type="button" class="basis-[50px] bg-[#969696] text-primary-text !ml-2 py-1 rounded !text-xs font-bold flex justify-center gap-1">
            <span>全站</span>
            <i v-if="showInputDropdown" class="bi bi-caret-up-fill"></i>
            <i v-else class="bi bi-caret-down-fill"></i>
          </button>
          <div class="flex-1 px-2">
            <input type="text" placeholder="5070ti" class="placeholder:text-sm placeholder:font-semibold placeholder-[#cccccc]">
          </div>
          <button class="basis-[32px] bg-main text-primary-text !rounded-lg w-[32px] h-[32px] !mr-1">
            <i data-feather="search" class="w-[15px] h-[15px] stroke-3 stroke-[#fff] mx-auto"></i>
          </button>
        </form>
        <div class="!text-xs mt-1.5 flex gap-3">
          <a class="!text-primary-text hover:!text-primary-text-hover !no-underline cursor-pointer">電競耳機</a>
          <a class="!text-primary-text hover:!text-primary-text-hover !no-underline cursor-pointer">行車記錄器</a>
          <a class="!text-primary-text hover:!text-primary-text-hover !no-underline cursor-pointer">行動電源</a>
          <a class="!text-primary-text hover:!text-primary-text-hover !no-underline cursor-pointer">除濕機</a>
          <a class="!text-primary-text hover:!text-primary-text-hover !no-underline cursor-pointer">筆電</a>
        </div>
        <div v-if="showInputDropdown" class="absolute top-13 w-[540px] h-[240px] bg-[#fff] rounded">
          <div class="grid grid-cols-5 h-full justify-center items-center">
            <button 
              v-for="button in inputDropdown"
              :key="button"
              class="cursor-pointer w-[88px] h-[40px] justify-self-center bg-[#f1f1f1] !rounded-full font-bold first:bg-[#fff] first:text-[#0090eb] first:border first:border-[#0090eb] hover:bg-[#fff] hover:text-[#0090eb] hover:border hover:border-[#0090eb]">
              {{ button }}
            </button>
          </div>
        </div>
      </div>
    </div>

    <div>
      
    </div>
  </div>
</template>

<style scoped>

</style>