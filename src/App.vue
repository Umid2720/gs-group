<script setup>
import top from './components/navbar/top.vue'
import IconPhone from './assets/icons/IconPhone.vue'
import IconHeart from './assets/icons/IconHeart.vue'
import IconShopping from './assets/icons/IconShopping.vue'
</script>

<template>
  <top />
  <header>
    <nav class="wrapper mx-auto flex items-center py-5 relative px-4 bb">
      <button class="relative group cursor-pointer h-5 w-6 inline md:hidden">
        <span
          class="w-6 h-0.5 rounded bg-black duration-300 left-0 inline-block group-hover:rotate-45 group-hover:top-2 absolute top-0"
        ></span>
        <span
          class="w-6 h-0.5 rounded bg-black duration-300 left-0 inline-block absolute group-hover:-rotate-45 group-hover:top-2"
        ></span>
        <span
          class="w-6 h-0.5 rounded bg-black duration-1000 left-0 inline-block absolute bottom-0 group-hover:hidden"
        ></span>
      </button>

      <a
        href="#"
        class="absolute right-4 -top-8 lg:-top-9 text-[12px] lg:text-[16px] underline font-medium tracking-[1.92px] lg:tracking-[2%] hidden md:inline text-white"
        >Обратный звонок</a
      >
      <a href="/" class="hidden md:inline">
        <img src="logo.png" alt="logo" />
      </a>

      <ul class="hidden md:flex items-center ml-16 lg:ml-24 gap-x-8 text-sm lg:text-xl main-color">
        <li>
          <router-link to="/" class="">Главная</router-link>
        </li>
        <li>Каталог</li>
        <li>
          <router-link to="/">Оптовая продажа</router-link>
        </li>
        <li>
          <router-link to="/">О нас</router-link>
        </li>
      </ul>
      <ul class="flex items-center ml-auto">
        <li class="items-end md:flex hidden">
          <IconPhone class="w-5 h-5 text-blue-500" />
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
  .bb{
    box-shadow: 0px -1px 0px 0px #C4CDD5 inset;
  }
</style>