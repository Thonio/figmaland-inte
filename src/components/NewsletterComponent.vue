<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';
import TextFieldComponent from './TextFieldComponent.vue';
import TitleComponent from './TitleComponent.vue';
</script>

<template>
  <div class="container mx-auto mb-[43px]">
    <div class="flex justify-center items-center gap-[50px]">
      <div class="order-2 ml-[63px] max-w-[544px]">
        <span class="font-[Graphik-bold] text-[20px]">At your fingertips</span>
        <TitleComponent>Lightning fast prototyping</TitleComponent>
        <span class="font-[Graphik-bold] text-[20px]">Subscribe to our Newsletter</span>
        <p class="text-[18px] mb-[60px]">Available exclusivery on Figmaland</p>
        <div>
          <TextFieldComponent type="text" name="newsletter" placeholder="Your Email" class="mr-[12px]" />
          <CtaComponent>Subscribe</CtaComponent>
        </div>
      </div>
      <div class="order-1">
        <img src="../../public/newsletter.svg" alt="#" />
      </div>
    </div>
  </div>
</template>
