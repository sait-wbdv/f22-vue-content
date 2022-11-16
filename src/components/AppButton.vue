<script setup>
defineProps({
  text: String,
  bgColor: {
    type: String,
    default: "bg-purple-500",
  },

  colors: {
    type: Array,
  },
});
</script>
<template>
  <button :class="bgColor" class="m-2 rounded-md px-4 py-2 text-white">
    {{ text }}
  </button>
</template>
