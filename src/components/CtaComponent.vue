<script setup lang="ts">
const props = defineProps({
  large: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <button :class="[props.large ? 'min-w-[238px]' : '']"
    class="text-white bg-[#2091F9] py-[16px] px-[38px] rounded-full">
    <slot></slot>
  </button>
</template>
