<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';
import TitleComponent from './TitleComponent.vue';
const listPartners = [
  {
    name: 'Client name',
    url: '../../public/google.svg'
  },
  {
    name: 'Client name',
    url: '../../public/amazon.svg'
  },
  {
    name: 'Client name',
    url: '../../public/microsoft.svg'
  },
  {
    name: 'Client name',
    url: '../../public/uber.svg'
  },
  {
    name: 'Client name',
    url: '../../public/dropbox.svg'
  },
  {
    name: 'Client name',
    url: '../../public/google.svg'
  },
  {
    name: 'Client name',
    url: '../../public/uber.svg'
  },
  {
    name: 'Client name',
    url: '../../public/amazon.svg'
  },
]
</script>

<template>
  <div class="container mx-auto mt-[120px] mb-[80px]">
    <div class="text-center mx-[20px] mb-[80px]">
      <TitleComponent>Partners</TitleComponent>
      <p class="text-[28px]">Most calendars are designed for teams. <br /> Slate is designed for freelancers</p>
    </div>
    <div class="flex max-w-[1078px] justify-center mx-auto mb-[80px] flex-wrap">
      <div v-for="partner in listPartners" class="text-center mx-[40px] my-[25px]">
        <p class="text-[15px] mb-[15px]">{{ partner.name }}</p>
        <img :src="partner.url" alt="#" />
      </div>
    </div>
    <div class="text-center">
      <CtaComponent :large="true" :bold="true">Try for free</CtaComponent>
    </div>
  </div>
</template>
