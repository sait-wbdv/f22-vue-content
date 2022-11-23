<script setup>
defineProps({
  url: {
    type: String,
    default: "#",
  },
});
</script>
<template>
  <a
    :href="url"
    class="underline-offset-4 hover:text-blue-500 hover:underline"
    ><slot></slot
  ></a>
</template>
