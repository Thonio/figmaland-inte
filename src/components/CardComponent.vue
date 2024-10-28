<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';

const props = defineProps({
  popular: {
    tyre: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <div
    :class="[props.popular ? 'bg-[#2091F9]' : 'bg-white', { 'py-[83px]': props.popular }, { 'text-white': props.popular }, { 'border-white': props.popular }]"
    class="rounded-lg max-w-[335px] text-center p-[40px] border border-solid">
    <div class="mb-[30px]">
      <h3 class="font-['Graphik-bold'] text-[20px] uppercase">
        <slot name="title"></slot>
      </h3>
      <p class="text-[16px]">
        <slot name="desicription"></slot>
      </p>
    </div>
    <div class="flex justify-center items-center gap-[10px] mb-[30px]">
      <div class="font-['Graphik-bold'] leading-[100%] text-[74px] uppercase">
        <slot name="price"></slot>
      </div>
      <div class="text-left">
        <div class="font-['Graphik-bold'] text-[20px]">$</div>
        <div class="text-[16px]">Per month</div>
      </div>
    </div>
    <div class="flex flex-col gap-[20px] mb-[30px]">
      <slot name="list"></slot>
    </div>
    <CtaComponent :white="props.popular" :large="true">Order now</CtaComponent>
  </div>
</template>
