<script setup lang="ts">
import CtaComponent from './CtaComponent.vue';
</script>

<template>
  <div class="relative overflow-hidden">
    <div class="flex flex-col min-h-[930px] bg-cover bg-no-repeat bg-bottom bg-[url('../../public/header.png')]">
      <div class="container mx-auto grow flex justify-center items-center">
        <div class="text-white text-center">
          <div class="max-w-[790px]">
            <h1 class="font-[Graphik] text-[48px] mx-[32px] mb-[22px] md:font-[Graphik-bold] md:text-[74px]">The best
              products
              start with
              Figma</h1>
            <p class="text-[28px] mx-[5px]">Most calendars are designed for teams. Slate is designed for freelancers</p>
          </div>
          <div class="my-[60px]">
            <CtaComponent :large="true">Try for Free</CtaComponent>
          </div>
        </div>
      </div>
    </div>
    <div class="arr-btm md:border-top-[21vh]">
    </div>
  </div>
</template>

<style scoped>
.arr-btm {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  width: 0;
  height: 0;
  border-top: 10vh solid transparent;
  border-left: 50vw solid white;
  border-right: 50vw solid white;
  border-bottom: 0 solid white;
}
</style>
