<script setup lang="ts">
import { ref } from 'vue';
import TitleComponent from './TitleComponent.vue';

const featureList = [
  {
    img: '../../public/form.svg',
    title: 'OpenTyp features Variable fonts',
    description: 'Slate helps you see how many more days you need to work to reach your financial goal.'
  },
  {
    img: '../../public/pencil.svg',
    title: 'Design with real data',
    description: 'Slate helps you see how many more days you need to work to reach your financial goal.'
  },
  {
    img: '../../public/paint.svg',
    title: 'Fastest way to take action',
    description: 'Slate helps you see how many more days you need to work to reach your financial goal.'
  }
]
const urlVideo = ref('')
const videoPlayed = ref(false)

const playVideo = () => {
  urlVideo.value = 'https://www.youtube.com/embed/-J9FuvPmMoI?autoplay=1'
  videoPlayed.value = true
}
</script>

<template>
  <div class="container mx-auto py-[80px] md:py-[115px]">
    <div class="text-center mb-[90px]">
      <TitleComponent>Features</TitleComponent>
      <p class="text-[28px]">Most calendars are designed for teams. <br />Slate is designed for freelancers</p>
    </div>
    <div class="flex flex-col mb-[52px] md:mb-0">
      <div class="md:order-2">
        <div v-if="videoPlayed" class="video-container mb-[70px]">
          <iframe width="560" height="315" :src="urlVideo" title="YouTube video player" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
        <div v-if="!videoPlayed" class="max-w-[1178px] pb-[70.25%] md:pb-[45%] mx-auto">
          <div class="video-thumbnail" @click="playVideo">
            <img src="../../public/video_screen.jpg" alt="#" class="thmbnail-image" />
            <div class="play-button size-[61px] md:size-[187px]"></div>
          </div>
        </div>
      </div>
      <div class="flex flex-col md:order-1 md:grid md:grid-cols-3 max-w-[870px] mx-auto gap-[52px]">
        <div v-for="feature in featureList" class="text-center w-[252px]">
          <img :src="feature.img" class="mx-auto mb-[10px]" />
          <h3 class="font-['Graphik-bold'] text-[20px] mb-[20px]">{{ feature.title }}</h3>
          <p class="text-[18px]">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.video-container {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%;
  height: 0;
  overflow: hidden;
}

.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none;
}

.video-thumbnail {
  position: absolute;
  width: 100%;
  max-width: 1178px;
  cursor: pointer;
}

.thmbnail-image {
  width: 100%;
  display: block;
}

.play-button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: url('../../public/play_button.svg') no-repeat center center;
  background-size: contain;
}
</style>
