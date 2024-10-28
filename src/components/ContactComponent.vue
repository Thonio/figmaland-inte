<script setup lang="ts">
import TextFieldComponent from './TextFieldComponent.vue';
import TitleComponent from './TitleComponent.vue';
import CtaComponent from './CtaComponent.vue';
import 'leaflet/dist/leaflet.css';
import { onMounted } from 'vue'
import L from 'leaflet'

const url = 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png';
const attribution = '© OpenStreetMap contributors';
const addressList = [
  {
    img: '../../public/marker.svg',
    address: '6386 Spring St Undefined Anchorage, Georgia 12473 United States'
  },
  {
    img: '../../public/phone.svg',
    address: '(843) 555-130'
  },
  {
    img: '../../public/mail.svg',
    address: 'willie.jennings@example.com'
  }
]
const socialLinks = [
  {
    img: '../../public/tweet_blue.svg',
    link: '#',
    title: 'X'
  },
  {
    img: '../../public/facebook_blue.svg',
    link: '#',
    title: 'Facebook'
  },
  {
    img: '../../public/linkedin_blue.svg',
    link: '#',
    title: 'Linkedin'
  }
]

onMounted(() => {
  const map = L.map('map').setView([51.505, -0.09], 13)

  L.tileLayer(url, {
    maxZoom: 19,
    attribution: attribution
  }).addTo(map)

  L.marker([51.5, -0.09]).addTo(map)
    .bindPopup('Test')
    .openPopup()
})
</script>

<template>
  <div class="container mx-auto mt-[153px] mb-[100px]">
    <div class="text-center mx-[20px]">
      <TitleComponent>Contact us</TitleComponent>
      <p class="text-[28px] mb-[60px]">Most calendars are designed for teams. <br />Slate is designed for freelancers
      </p>
    </div>
    <div class="flex flex-col md:flex-row max-w-[1228px] mx-auto gap-[50px]">
      <div class="md:order-2 flex flex-col py-[29px]">
        <div class="md:order-3 flex gap-[24px] justify-center md:justify-start mb-[50px] md:mb-0">
          <div v-for="social in socialLinks"><a class="flex justify-center w-[41px] h-[41px]" :href="social.link"
              :title="social.title"><img class="w-[33px]" :src="social.img" alt="#" /></a></div>
        </div>
        <div class="hidden md:block md:order-2 my-[50px]">
          <div id="map" class="w-[516px] h-[323px] mx-auto"></div>
        </div>
        <div class="md:order-1 flex flex-col md:flex-row gap-[15px] items-start mx-[30px] md:items-center">
          <div v-for="address in addressList" class="flex md:block max-w-[313px] text-left md:text-center">
            <img :src="address.img" alt="#" class="mr-[20px] md:mx-auto mb-[10px]" />
            <p class="text-[16px]">{{ address.address }}</p>
          </div>
        </div>
      </div>
      <div class="md:order-1 mx-[20px] px-[50px] py-[52px] w-auto md:w-[453px] border rounded-xl shadow-lg">
        <h3 class="font-['Graphik-bold'] text-[20px] text-center mb-[45px]">Contact us</h3>
        <form class="flex flex-col gap-[45px]">
          <TextFieldComponent :fullwidth="true" type="text" name="name" placeholder="Your name" />
          <TextFieldComponent :fullwidth="true" type="text" name="email" placeholder="Your mail" />
          <TextFieldComponent :fullwidth="true" type="area" name="name" placeholder="Your message" />
          <div>
            <CtaComponent>Send</CtaComponent>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
