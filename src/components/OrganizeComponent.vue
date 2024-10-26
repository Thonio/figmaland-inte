<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';
import TitleComponent from './TitleComponent.vue';
</script>

<template>
  <div class="my-[226px] mx-auto container">
    <div class="flex justify-center items-center gap-[50px]">
      <div>
        <TitleComponent>Fastest way to <br /> organize</TitleComponent>
        <p class="text-[28px] mb-[60px]">Most calendars are designed for teams. <br />Slate is designed for freelancers
        </p>
        <CtaComponent :large="true" :bold="true">Try for Free</CtaComponent>
      </div>
      <div>
        <img src="../../public/computer.svg" />
      </div>
    </div>
  </div>
</template>
