<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';
import TextFieldComponent from './TextFieldComponent.vue';
import TitleComponent from './TitleComponent.vue';
</script>

<template>
  <div class="container mx-auto mb-[43px]">
    <div class="mx-[20px]">
      <div class="text-center md:text-left md:float-right md:ml-[63px] max-w-[544px]">
        <span class="font-[Graphik-bold] text-[20px]">At your fingertips</span>
        <TitleComponent>Lightning fast prototyping</TitleComponent>
      </div>
      <div class="mb-[60px] md:mb-0 md:float-left">
        <img src="../../public/newsletter.svg" alt="#" />
      </div>
      <div class="text-center md:text-left md:float-right max-w-[544px] md:w-1/2">
        <span class="font-[Graphik-bold] text-[20px]">Subscribe to our Newsletter</span>
        <p class="text-[18px] mb-[40px] md:mb-[60px]">Available exclusivery on Figmaland</p>
        <TextFieldComponent type="text" name="newsletter" placeholder="Your Email"
          class="w-full mb-[12px] md:w-auto mr-[12px]" />
        <CtaComponent class="w-full md:w-auto">Subscribe</CtaComponent>
      </div>
    </div>
    <div class="clear-both"></div>
  </div>
</template>
