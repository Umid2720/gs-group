<script setup>
import top from './components/navbar/top.vue'
import IconPhone from './assets/icons/IconPhone.vue'
import IconHeart from './assets/icons/IconHeart.vue'
import IconShopping from './assets/icons/IconShopping.vue'
</script>

<template>
  <top />
  <header>
    <nav class="wrapper mx-auto flex items-center py-5 main-color">
      <a href="/">
        <img src="logo.png" alt="logo" />
      </a>
      <ul class="flex items-center ml-[101px] gap-x-8 text-xl">
        <li>
          <router-link to="/">Главная</router-link>
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
        <li class="flex items-end">
          <IconPhone class="w-5 h-5 text-blue-500" />
          <a href="tel:+79665588499" class="text-lg">+7 (966) 55 88 499</a>
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
