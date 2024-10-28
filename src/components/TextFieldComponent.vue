<script setup lang="ts">
const props = defineProps({
  type: {
    type: String,
    required: true,
    default: 'text'
  },
  name: {
    type: String,
    required: true,
    default: ''
  },
  placeholder: {
    type: String,
    required: false,
    default: ''
  },
  fullwidth: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <input v-if="props.type !== 'area'" :class="{ 'w-full': props.fullwidth }"
    class="border-[#E8E8E8] bg-[#f5f5f5] border rounded-full py-[14px] px-[38px]" :type="props.type" :name="props.name"
    :placeholder="props.placeholder" />
  <textarea :class="{ 'w-full': props.fullwidth }"
    class="border-[#E8E8E8] bg-[#F5F5F5] border h-[193px] py-[16px] px-[38px]" v-else :name="props.name"
    :placeholder="props.placeholder" />
</template>
