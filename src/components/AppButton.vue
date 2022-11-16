<script setup>
defineProps({
  text: String,
  bgColor: {
    type: String,
    default: "bg-purple-500",
  },
  src: {
    type: String,
  },
  altText: String,
  num: {
    type: Number,
    default: 3,
  },
});
</script>
<template>
  <button :class="bgColor" class="m-2 rounded-md px-4 py-2 text-white">
    <img :src="src" :alt="altText" />{{ text }} {{ num }}
  </button>
</template>
