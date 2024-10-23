<script setup lang="ts">
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
    link: '#',
    title: 'X'
  },
  {
    img: '../../public/facebook.svg',
    link: '#',
    title: 'Facebook'
  },
  {
    img: '../../public/linkedin.svg',
    link: '#',
    title: 'Linkedin'
  }
]
</script>

<template>
  <div class="relative">
    <div class="z-[999] absolute w-full">
      <div class="container w-full mx-auto">
        <div class="grid grid-cols-3 mx-auto py-[39px] px-[40px] max-w-[1210px]">
          <div class="flex items-center z-1">
            <ul class="flex gap-[21px] item-center">
              <li v-for="link in links" class="p-[10px]"><a :href="link.link" class="text-white text-[15px]">{{
                link.name }}</a>
              </li>
            </ul>
          </div>
          <div class="flex justify-center items-center">
            <img src="../../public/logo.svg" alt="logo" />
          </div>
          <div class="flex justify-end items-center">
            <ul class="flex gap-[24px]">
              <li v-for="social in socialLinks"><a class="flex justify-center w-[41px] h-[41px]" :href="social.link"
                  :title="social.title"><img class="w-[33px]" :src="social.img" alt="#" /></a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
