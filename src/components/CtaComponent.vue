<script setup lang="ts">
const props = defineProps({
  large: {
    type: Boolean,
    required: false,
    default: false
  },
  bold: {
    type: Boolean,
    required: false,
    default: false,
  },
  white: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <button
    :class="[{ 'min-w-[238px]': props.large, 'font-[\'Graphik-bold\']': props.bold }, props.white ? 'bg-white' : 'bg-[#2091F9]', props.white ? 'text-[#2091F9]' : 'text-white']"
    class="py-[16px] px-[38px] rounded-full">
    <slot></slot>
  </button>
</template>
