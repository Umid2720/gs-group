<script setup>
import { ref } from 'vue'
import top from './components/navbar/top.vue'
import IconPhone from './assets/icons/IconPhone.vue'
import IconHeart from './assets/icons/IconHeart.vue'
import IconShopping from './assets/icons/IconShopping.vue'

const menu = ref(false)
</script>

<template>
  <top />
  <header>
    <nav class="wrapper mx-auto flex items-center py-5 relative px-4 bb">
      <button class="relative group cursor-pointer h-5 w-6 inline md:hidden" @click="menu = !menu">
        <span
          :class="[
            menu ? 'rotate-45 top-2' : 'top-0',
            'w-6 h-0.5 rounded bg-black duration-300 left-0 inline-block absolute'
          ]"></span>
        <span
          :class="[
            menu ? '-rotate-45 top-2' : '',
            'w-6 h-0.5 rounded bg-black duration-300 left-0 inline-block absolute'
          ]"
        ></span>
        <span
          :class="[
            menu ? 'w-0' : 'w-6',
            'h-0.5 rounded bg-black duration-200 left-0 inline-block absolute bottom-0'
          ]"
        ></span>
      </button>

      <a
        v-show="menu"
        href="#"
        class="md:absolute right-4 fixed bottom-10 md:-top-8 lg:-top-9 text-[12px] lg:text-[16px] underline font-medium tracking-[1.92px] lg:tracking-[2%] md:inline md:text-white text-[#4295E4] z-10"
        >Обратный звонок</a
      >
      <a href="/" class="hidden md:inline">
        <img src="logo.png" alt="logo" />
      </a>

      <ul
        v-show="menu"
        class="absolute md:static bg-green-00 h-screen md:h-auto md:bg-transparent w-full left-0 px-4 md:w-auto -bottom-[469px] md:flex items-center ml-0 md:ml-16 lg:ml-24 gap-x-8 text-sm lg:text-xl main-color space-y-4 md:space-y-0 duration-300 pt-4 md:p-0"
      >
        <li
          class="border-b pb-4 w-full leading-[26px] md:leading-normal md:border-0 md:pb-0 md:w-auto"
        >
          <router-link to="/" class="">Главная</router-link>
        </li>
        <li
          class="border-b pb-4 w-full leading-[26px] md:leading-normal md:border-0 md:pb-0 md:w-auto"
        >
          Каталог
        </li>
        <li
          class="border-b pb-4 w-full leading-[26px] md:leading-normal md:border-0 md:pb-0 md:w-auto"
        >
          <router-link to="/">Оптовая продажа</router-link>
        </li>
        <li
          class="border-b pb-4 w-full leading-[26px] md:leading-normal md:border-0 md:pb-0 md:w-auto"
        >
          <router-link to="/">О нас</router-link>
        </li>
      </ul>
      <ul class="flex items-center ml-auto">
        <li class="items-end flex fixed bottom-[38px] md:static left-4 z-10" v-show="menu">
          <IconPhone class="w-5 h-5 text-blue-500 mr-2" />
          <a href="tel:+79665588499" class="text-sm lg:text-lg">+7 (966) 55 88 499</a>
        </li>
        <li class="ml-7 mr-6">
          <IconHeart class="w-6 h-6" />
        </li>
        <li>
          <IconShopping class="w-6 h-6" />
        </li>
      </ul>
    </nav>
  </header>

  <RouterView />
</template>

<style lang="css">
.bb {
  box-shadow: 0px -1px 0px 0px #c4cdd5 inset;
}
</style>
