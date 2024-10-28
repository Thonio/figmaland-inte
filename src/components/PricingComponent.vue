<script setup lang="ts">
import CardComponent from './CardComponent.vue';
import TitleComponent from './TitleComponent.vue';
</script>

<template>
  <div class="bg-[#252B42] py-[100px]">
    <div class="container mx-auto">
      <div class="text-center mx-[20px]">
        <TitleComponent class="text-white">Pricing</TitleComponent>
        <p class="text-[28px] mb-[60px] text-white">Most calendars are designed for teams. <br />Slate is designed for
          freelancers
        </p>
      </div>
      <div class="flex flex-col md:flex-row gap-[50px] justify-center items-center">
        <CardComponent>
          <template #title>Free</template>
          <template #desicription>Organize across all <br /> apps by hand</template>
          <template #price>0</template>
          <template #list>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
          </template>
        </CardComponent>
        <CardComponent :popular="true">
          <template #title>Standard</template>
          <template #desicription>Organize across all <br /> apps by hand</template>
          <template #price>10</template>
          <template #list>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
          </template>
        </CardComponent>
        <CardComponent>
          <template #title>Business</template>
          <template #desicription>Organize across all <br /> apps by hand</template>
          <template #price>99</template>
          <template #list>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
            <div>Pricing features</div>
          </template>
        </CardComponent>
      </div>
    </div>
  </div>
</template>
