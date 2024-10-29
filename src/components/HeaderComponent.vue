<script setup lang="ts">
import { ref } from 'vue';

const links = [
  {
    name: 'Home',
    link: '#'
  },
  {
    name: 'Product',
    link: '#'
  },
  {
    name: 'Pricing',
    link: '#'
  },
  {
    name: 'About',
    link: '#'
  },
  {
    name: 'Contact',
    link: '#'
  }
]
const socialLinks = [
  {
    img: '../../public/tweeter.svg',
    img_mobile: '../../public/tweet_blue.svg',
    link: '#',
    title: 'X'
  },
  {
    img: '../../public/facebook.svg',
    img_mobile: '../../public/facebook_blue.svg',
    link: '#',
    title: 'Facebook'
  },
  {
    img: '../../public/linkedin.svg',
    img_mobile: '../../public/linkedin_blue.svg',
    link: '#',
    title: 'Linkedin'
  }
]
const show = ref(false)
</script>

<template>
  <div class="relative md:block">
    <div class="z-[999] absolute w-full">
      <div class="container w-full mx-auto">
        <div class="grid grid-cols-2 md:grid-cols-3 mx-auto p-[17px] md:p-[40px] max-w-[1210px]">
          <div class="hidden md:flex items-center z-10">
            <ul class="flex gap-[21px] item-center">
              <li v-for="link in links" class="p-[10px]"><a :href="link.link" class="text-white text-[15px]">{{
                link.name }}</a>
              </li>
            </ul>
          </div>
          <div class="flex justify-center items-center">
            <img src="../../public/logo.svg" alt="logo" />
          </div>
          <div class="flex justify-end items-center md:hidden">
            <button @click="show = !show"><img src="../../public/burger.svg" alt="#" /></button>
          </div>
          <div class="hidden md:flex justify-end items-center">
            <ul class="flex gap-[24px]">
              <li v-for="social in socialLinks"><a class="flex justify-center w-[41px] h-[41px]" :href="social.link"
                  :title="social.title"><img class="w-[33px]" :src="social.img" alt="#" /></a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <Transition>
      <div v-if="show" class="bg-white fixed w-full h-full z-[999] p-[40px]">
        <div class="text-right"><button @click="show = !show"><img class="size-[45px]" src="../../public/close.png"
              alt="#"></button></div>
        <ul class="flex flex-col gap-[21px] item-center">
          <li v-for="link in links" class="p-[10px]"><a :href="link.link" class="text-black text-[15px]">{{
            link.name }}</a>
          </li>
        </ul>
        <ul class="flex gap-[24px] justify-center mt-[70px]">
          <li v-for="social in socialLinks"><a class="flex justify-center w-[41px] h-[41px]" :href="social.link"
              :title="social.title"><img class="w-[33px]" :src="social.img_mobile" alt="#" /></a></li>
        </ul>
      </div>
    </Transition>
  </div>
</template>

<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
