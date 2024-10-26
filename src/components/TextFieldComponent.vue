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
  }
})
</script>

<template>
  <input v-if="props.type !== 'area'" class="bg-[#E8E8E8] rounded-full py-[16px] px-[38px]" :type="props.type"
    :name="props.name" :placeholder="props.placeholder" />
  <textarea v-else :name="props.name" :placeholder="props.placeholder" />
</template>
