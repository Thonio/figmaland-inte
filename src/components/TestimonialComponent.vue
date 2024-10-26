<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';
import TitleComponent from './TitleComponent.vue';
</script>

<template>
  <div class="container mx-auto py-[100px] text-center">
    <TitleComponent class="mb-[80px]">Testimonials</TitleComponent>
    <div class="text-center max-w-[987px] mx-auto">
      <img class="mx-auto mb-[50px]" src="../../public/ibm.svg" alt="ibm" />
      <p class="text-[28px] mb-[50px]">Most calendars are designed for teams. Slate is designed for freelancers who want
        a simple way to plan their schedule </p>
      <div class="flex max-w-[186px] mx-auto mb-[80px]">
        <div class="size-[50px] rounded-full overflow-hidden mr-[13px]">
          <img src="../../public/profile.svg" alt="profile" />
        </div>
        <div class="text-[15px] text-left">Organize across <br />Ui designer</div>
      </div>
      <div>
        <CtaComponent :large="true" :bold="true">More Testimonials</CtaComponent>
      </div>
    </div>
  </div>
</template>
