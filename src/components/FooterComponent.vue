<script setup lang="ts">
const pageList = [
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
  },
]
const nameList = [
  {
    name: 'Eleanor Edwards',
    link: '#'
  },
  {
    name: 'Ted Robertson',
    link: '#'
  },
  {
    name: 'Annette Russell',
    link: '#'
  },
  {
    name: 'Jennie Mickinney',
    link: '#'
  },
  {
    name: 'Gloria Richards',
    link: '#'
  },
]
const secondList = [
  {
    name: 'Philip Jones',
    link: '#'
  },
  {
    name: 'Product',
    link: '#'
  },
  {
    name: 'Collin Russell',
    link: '#'
  },
  {
    name: 'Marvin Hawckins',
    link: '#'
  },
  {
    name: 'Bruce Simmmons',
    link: '#'
  },
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
  <footer class="bg-[#252B42] text-white text-center md:text-left">
    <div class="max-w-[991px] mx-auto py-[150px] justify-between flex flex-col md:flex-row">
      <div class="md:grid grid-cols-3 w-[100%] md:w-[582px] gap-[20px]">
        <div class="mb-[73px]">
          <h3 class="font-['Graphik-bold'] text-[20px] mb-[25px]">Pages</h3>
          <ul>
            <li v-for="page in pageList" class="mb-[16px]">
              <a href="#" class="text-[15px]">{{ page.name }}</a>
            </li>
          </ul>
        </div>
        <div class="mb-[73px]">
          <h3 class="font-['Graphik-bold'] text-[20px] mb-[25px]">Tomothy</h3>
          <ul>
            <li v-for="name in nameList" class="mb-[16px]">
              <a href="#" class="text-[15px]">{{ name.name }}</a>
            </li>
          </ul>
        </div>
        <div class="mb-[73px]">
          <h3 class="font-['Graphik-bold'] text-[20px] mb-[25px]">Jane Black</h3>
          <ul>
            <li v-for="second in secondList" class="mb-[16px]">
              <a href="#" class="text-[15px]">{{ second.name }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="mx-[67px] md:mx-0">
        <div class="flex items-center gap-[15px] mb-[10px]">
          <img src="../../public/marker_white.svg" alt="#" />
          <p>7480 Mockingbird Hill</p>
        </div>
        <div class="flex items-center gap-[15px]">
          <img src="../../public/phone_white.svg" alt="#" />
          <p>(239) 555-139</p>
        </div>
        <div class="py-[27px]">
          <ul class="flex justify-center md:justify-start gap-[24px]">
            <li v-for="social in socialLinks"><a class="flex justify-center w-[41px] h-[41px]" :href="social.link"
                :title="social.title"><img class="w-[33px]" :src="social.img" alt="#" /></a></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>
